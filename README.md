PyDNSProxy
==========

PyDNSProxy Configuration.

Author
======

Jioh L. Jung (ziozzang@gmail.com)

License
=======

This code is under License of BSD.

Functions
=========

DNS Proxy + SNI/HTTP Proxy + Very Basic Authenticate

Environment
===========

This source is working with Python 3.4 + AsyncIO. you have to run in \*NIX include Linux as root permission.

Configuration
=============

on source code, there's 3 kind of configuration.

1. Authentication is on source code as IP list. if IP is in list or block, DNS and SNI proxy working. else, ith doesn't reply.
```
auth_list = ["10.2.3.4", "10.3.4.5"]  # per IP Auth.
auth_block = ["10.1.0.0/16", "10.98.76.0/24"] # Block by
```

2. or Passphase for SNIProxy Open. dns query of this Record, the gate will be open!
```
passphase = "open.the.gate.sesami"
```

3. Check the domain is really exist.
```
filter_exist_dns = True
```

on dns.conf file, you can control dns record what to reply fake one. see dns.conf file.


Special Thanks
==============

* Basic SNI Proxy code from Phus Lu <phus.lu@gmail.com> https://github.com/phuslu/sniproxy/
* DNSProxy code from Crypt0s's FakeDNS. https://github.com/Crypt0s/FakeDns
