👌 Tested on Zabbix 4.4, 5.0

🤝 (Based on https://github.com/Semeyn/monit_flussonic_in_zabbix from https://t.me/erlyvideo chat, but translated into English.)
# Flussonic monitoring for Zabbix
0. Clone this repository .
1. Import Template App Flussonic Service API.xml into your Zabbix web interface .
2. Add this new Template to your Flussonic servers.
3. Copy all files from scripts dirrectory into your Flussonic server with path /etc/zabbix/flussonic-scripts .
4. Add your variables into /etc/zabbix/flussonic-scripts/flussonic.cfg
API_IP="" 
API_USER=""
API_PASS=""
5. On Flussonic server run ln -s /etc/zabbix/flussonic-scripts/flussonic_cron /etc/cron.d/flussonic_cron .
6. Move flussonic.conf file to /etc/zabbix/zabbix_agentd.d/ or make symbol link like this: ln -s /etc/zabbix/flussonic-scripts /etc/zabbix/zabbix_agentd.d/flussonic.conf .
7. Run service zabbix-agent restart
8. Whait about 1 min and we can see data from your Flussonic server in Zabbix.

⚠️ PS: There is no graphs by default. You can add them by yourself.

