# cupsd
CUPS Daemon for Raspberry Pi

Original work: https://github.com/olbat/dockerfiles/tree/master/cupsd.

I made following changes:
- Change base image to Debian stretch (for ARM64) because I want to use it on my RPI3
- Create docker-compose.yml

To run it:
- Without docker compose: `docker run -d -p 631:631 -v /var/run/dbus:/var/run/dbus --device /dev/bus/usb:/dev/bus/usb --name cupsd carnel/cupsd`
- With docker compose: `docker-compose up -d`
