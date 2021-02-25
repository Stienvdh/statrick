## Connect to your DevNet Sandbox using your AnyConnect client

The credentials were emailed to you after reserving a Recommended Code IOS XE sandbox on https://devnetsandbox.cisco.com/RM/Topology

## Clone the repo

Run in terminal: 
```
$ git clone https://github.com/Stienvdh/statrick.git
$ cd statrick
```

## Activate virtual environment

Run in terminal: 
```
$ cd intro-ansible
$ python -m venv venv
$ source venv/bin/activate
$ pip install -r requirements.txt
```

## Run mission

Run in terminal: 
```
$ cd ansible-04-mission
$ ansible-playbook ansible-04-mission/04-mission.yaml
```

Your output should end with something like this:

```
TASK [display value of "myint" variable] ***************************************
ok: [10.10.20.48] => {
    "myint[\"stdout_lines\"][0]": [
        "Interface              IP-Address      OK? Method Status                Protocol",
        "GigabitEthernet1       10.10.20.48     YES NVRAM  up                    up      ",
        "GigabitEthernet2       unassigned      YES NVRAM  administratively down down    ",
        "GigabitEthernet3       unassigned      YES NVRAM  administratively down down    ",
        "Loopback1167           10.67.11.1      YES manual up                    up      ",
        "Loopback1267           10.67.12.1      YES manual up                    up      ",
        "Loopback1367           10.67.13.1      YES manual up                    up      ",
        "Loopback1467           10.67.14.1      YES manual up                    up"
    ]
}
```

## Push your shiny new config to your own public repo
This is explained beautifully in the readme.md file of https://github.com/GShuttleworth/Cisco-IOS-XE-config-to-Git

## Clean up your act

Run in terminal: 
```
$ ansible-playbook ansible-04-mission/04-lab-cleanup.yaml
```
