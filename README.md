# Alert Logic al-agent Cloud Init
Installs/Configures the Alert Logic Agent via cloud-init and 
Alert Logic [al_agents](https://github.com/alertlogic/al_agents) cookbook

## CloudInit
[CloudInit](http://cloudinit.readthedocs.org/) is the way to install something
onto cloud instances (i.e. amazon ec2).
You may find useful examples under [cloud-init](cloud-init/) directory.
In case of amazon ec2 just pass this .yml file as `user-data`, do not forget
to change `registration_key`. If you would like to route traffic through a SOCKS 
or HTTP proxy, set the `proxy_url` value to point to your specific proxy.
This will install chef-client to your instance, download this cookbook and
run `chef-solo`.

Note that in case of amazon ec2 `user-data` will be accessible to any
user from within this instance.



License and Authors
-------------------
License:
Distributed under the Apache 2.0 license.

Authors: Justin Early (jearly@alertlogic.com)
