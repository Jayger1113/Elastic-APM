# Elastic-Kibana

how to start

$cd elastic-apm/docker

$export TAG=7.2.0

$docker-compose -f docker-compose.yml -d

# Nginx (proxy port from 80 to kibana 5601)

$ sudo apt-get install nginx
$ sudo vim /etc/nginx/sites-available/default
$ copy & paste /docker/nginx.default
$ sudo systemctl enable nginx
$ sudo systemctl start nginx

# To check if nginx is working
$ sudo systemctl status nginx


# Thouble-shooting

elastic search
[1]: max virtual memory areas vm.max_map_count [65530] is too low, increase to at least [262144]

solution: sudo sysctl -w vm.max_map_count=262144 or add vm.max_map_count=262144 to "/etc/sysctl.conf" and restart
