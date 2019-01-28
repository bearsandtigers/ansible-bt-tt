# OVPN-TEST-TASK ansible role

Installs openvpn client on ubuntu xenial and applies a simple configuration for it

## Variables:

### global vars

certification authority certificate:
`ovpnc_ca:` <see vars/main.yml>

client's os codename to apply role on:
`ovpnc_os_codename: xenial`

openvpn server address to connect to,
can be redefined individually for each target 
in the host variables files
`ovpnc_server: 8.8.8.8`

openvpn tls auth property:
`ovpnc_tlsauth:` <see vars/main.yml>

fixed openvpn client version (in xenial) to install:
`ovpnc_version: 2.3.10-1ubuntu2.1`

### host vars

client's ssl certificate:
`ovpnc_cert:` <role default value is a stub string, 
proper value for each target host should be specified
in the corresponding host_vars file>          

client's ssl secret key:
`ovpnc_private_key:` <role default value is a stub string, 
proper value for each target host should be specified
in the corresponding host_vars file>

## Tags:

to enable autostart and push client config
`config`

to install openvpn via apt:
`install`


