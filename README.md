# Elastic-Kibana

how to start

$cd elastic-apm
$export TAG=7.2.0
$docker-compose -f docker-compose.yml -d

# Thouble-shooting

elastic search
[1]: max virtual memory areas vm.max_map_count [65530] is too low, increase to at least [262144]

solution: sudo sysctl -w vm.max_map_count=262144 or add vm.max_map_count=262144 to "/etc/sysctl.conf" and restart
