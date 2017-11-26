PKCS11-Proxy
=========

Role will install PKCS11 network proxy.  

Role Variables
--------------

```
pkcs11proxy_server: true                  # false will run client component
pkcs11_module: '/path/to/pkcs11.so'       # pkcs11 library to be served by proxy

pkcs11proxy_ip: "0.0.0.0"                 # server is open by default
pkcs11proxy_port: 2345

pkcs11proxy_server_ip: "1.2.3.4"          # client uses this for connection
pkcs11proxy_server_port: 2345
```

Example Playbook
----------------

```
- hosts: all
  become: yes
  vars:
    - pkcs11proxy_server: true
    - pkcs11_module: '/usr/lib/x86_64-linux-gnu/softhsm/libsofthsm2.so'
  roles:
    - ansible-role-pkcs11-proxy
```

License
-------

BSD
