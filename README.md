# Kathara Traffic Dumper

This tool allows dumping all the traffic produced by a Kathará network scenario on all the collision domains.
The script simply runs the scenario, attaching a device that dumps all the collision domains in the network.

## Pre-requirements

- Docker
- `python3` version >= 3.10

## Installing Kathará Python APIs

```bash
python3 -m pip install git+https://github.com/saghul/pyuv@master#egg=pyuv
python3 -m pip install kathara
```

More details [here](https://github.com/KatharaFramework/Kathara-Labs/tree/main/tutorials/python-api/getting-started)

## How does it work?

The tool uses the Kathará Python APIs to run a Kathará network scenario and to dump all the traffic produced on all the
collision domains of the scenario. To do so, the script adds a new device attached to all the collision domains which
dumps all the traffic. 

```bash
python3 main.py --network-scenario labs/kathara-lab_rip --dump-time 10
```

Dumped `.pcap` files can be found in the `pcaps` directory. 

