# PHP-Apache, mod status, prometheus and Grafana

Simple docker-compose with php-apache container with mod_status as virtualhost and the prometheus exporter.

To test it, i used a phpinfo document

I add prometheus and Grafana with the datasource and dashboards auto-imported

All containers used the "expose" parameter to use this port for the docker-networks, not linked with the node.

## Apache mod_status
The mod_status are enabled by default.<br>
I modified the "listen" ports, at file ~/apache-configs/ports.conf and create a new virtualhost to this port and only serve the apache metrics.<br> 
This virtualhost it's going to be used with the prometheus-apache-exporter

## All containers used

- Official PHP+Apache container
  - https://hub.docker.com/_/php
- Prometheus Apache Exporter
  - https://github.com/Lusitaniae/apache_exporter
  - https://hub.docker.com/repository/docker/danifernandezs/prometheus-apache-exporter
- Node Exporter Official container
  - https://hub.docker.com/r/prom/node-exporter
- Prometheus Official container
  - https://hub.docker.com/r/prom/prometheus
- Grafana Official container
  - https://hub.docker.com/r/grafana/grafana

## License

<img src="./img/by-sa.png">

This work is under [Creative Commons Attribution-ShareAlike 4.0 International License](http://creativecommons.org/licenses/by-sa/4.0/).

Please read the LICENSE files for more details.
