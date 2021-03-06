# resin-mdns-service

An example project to set up local services and advertise them over Avahi/mDNS.
It installs the Avahi daemon within the user container, and sets up two example
services as shown below.

**Important**: this will only work with resinOS 1.x devices! On resinOS 2.x
the system comes with Avahi, and instead of this project, you should see
[resin-avahi-dbus](https://github.com/resin-io-playground/resin-avahi-dbus) for
an example how to communicate with the system Avahi over dbus.

## TCP

A "Quote of the Day" service exposed on port 17 over TCP. You can test it by running

```Bash
nc <device-hostname>.local 17
```

## UDP

An Echo service exposed on port 7 over UDP. Can test it by running

```Bash
date | nc -u <device-hostname>.local 7
```

See more examples of Avahi services in the [ArchLinux Wiki](https://wiki.archlinux.org/index.php/avahi#Adding_services).

## License

Apache 2.0, see [LICENSE](./LICENSE).
