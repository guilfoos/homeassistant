# HOME ASSISTANT #

This Github repository is to help me maintain a known-good version I can roll-back to as I continue to improve my integrations. And a little bit of DR.

For others, I mostly edit in vi (I'm a bit of a dinosaur), but there is a nice HACS plugin that gives you an editor you can use on a Dashboard. When I add an integration and get everything working, I can commit the changes here so that if further tinkering breaks somethign I can recover.

I'll try to keep this readme fairly up-to-date, but no promises. As always, the details are in the commit logs. Currently moving house, so I'm rebuilding from scratch and will be adding hardware as I get new integrations set up.

** Environment **

All of my applications run in Docker containers. I've found it's much easier to maintain the environment - and migrate it to updated hardware - if configuration data is segretaged and software is kept independent. I can just move the configuration and data folders, copy the docker-compose.yml, and we are up and running. Some specifics for my Home Assistant setup; I'm running the offical Docker container, but have a MariaDB container set up to store the database, and an InfluxDB container set up to record timeseries data. I also have Grafana set up to build reporting dashboards. Not using it much yet, but we will get there. I can monitor my Docker container statistics in HA, and you can see that looking at the configuration I have a bunch of media management containers as well that are out-of-scope for this description.

** My hardware: **
- 1 RPi4 8GB, running Ubuntu on a 32GB SD card and a 8TB external HDD for docker configuration and media files. Home Assistant and all other helper applications run in Docker containers.

- Nortek USB Zigbee/ZWave hub

- 1 Sengled WiFi RGB bulb

- 1 TP-Link Kasa Smart switch (KP115)

- 1 Aqara Zigbee door/window sensor

- 2 Google Nest Hubs

- 2 Google Nest Mini

- 1 Google Nest Audio

- 1 Chromecast

More hardware to be listed as I get integrations set up at the new house.

** Custom Automations **

- Monitor washing machine power load and door state to know when clothes are clean and need to be moved to the dryer
