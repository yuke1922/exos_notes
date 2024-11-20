# General

## Port Stats Commands
- show port state
```exos
show ports <port>
show ports
```

- show port packet counters
```exos
show ports statistics wide port-number  #Press 0 in the output to clear counters
show ports statistics wide
show ports <port> statistics wide port-number
```

## RSTP Configuration
- Configure STP for RSTP, set priority, enable auto bind
```exos
disable stpd s0
configure stpd s0 mode dot1w
enable stpd s0
enable stpd s0 auto-bind <vlan>
```

## Basic VLAN Management

- Create VLANs and manage ports
```exos
create vlan v10-Dante tag 10
create vlan v20-NVX tag 20

configure vlan v10-Dante add ports 1-3 untagged
configure vlan v10-Dante add ports 6 tagged
configure vlan v20-NVX add ports 6 tagged
```