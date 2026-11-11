# Enterprise-Style Home Network Lab

Disclaimer: I used AI assistance while building this project and writing it up. I don’t claim to know every command or setting, and I’m still learning and developing my skills. As you read, please keep in mind that there may be mistakes, and that my setup may not match how professionals would do it. I built this lab mainly for fun and to learn, with the hope of one day landing a networking job. If you spot something I got wrong or could do better, I’d genuinely welcome the feedback.

Introduction:
A hands-on networking and Windows Server lab built from real Cisco hardware, used to practice what I'm studying and to build skills in Networking.

> **Status:** Phase 2 complete (VLANs and inter-VLAN routing, Day 2: 3 Nov 2026). Day 3 (10 Nov 2026) started on ACLs and switch hardening.

## Build log

| Day | What I built | Write-up |
|---|---|---|
| Day 1 (2 Nov 2026) | Flat network: router NAT, Windows Server with AD, DNS and DHCP, domain-joined clients | [Day 1](day1/README.md) · [build log](docs/day1-build-log.md) |
| Day 2 (3 Nov 2026) | VLANs, trunks, inter-VLAN routing on the multilayer switch, DHCP relay, restricted file share | [Day 2](day2/README.md) |
| Day 3 (10 Nov 2026) | Security VLAN 30 for a Swann NVR and camera, DHCP from the DC, ACLs in both directions, SSH-only management and unused ports shut down | [Day 3](day3/README.md) |

## Current topology

![Current topology](diagrams/day3-topology.png)

Network: VLAN 10 `10.0.10.0/24` · VLAN 20 `10.0.20.0/24` · VLAN 30 `10.0.30.0/24` · router link `10.0.99.0/30` · domain `johndom.csnt`

## Roadmap

- [x] Phase 1: flat network, router NAT, AD + DNS + DHCP, domain-joined clients
- [x] Phase 2: VLANs, trunks, inter-VLAN routing on the multilayer switch
- [ ] Phase 3: firewall VM (pfSense/OPNsense), ACLs, move NAT/policy to it
- [ ] Phase 4: hardening (SSH only, enable secret, port security, DHCP snooping), Group Policy, file shares
- [ ] Phase 5: monitoring and logging (syslog, SNMP)

## Repo layout

```
day1/       Day 1 write-up (flat network)
day2/       Day 2 write-up (VLANs, inter-VLAN routing, restricted share)
day3/       Day 3 write-up (security VLAN, ACLs, switch hardening)
configs/    device configs, one set per day
diagrams/   topology diagrams (image + Packet Tracer file), one per day
docs/       build logs
images/     photos and screenshots used in the write-ups
```
