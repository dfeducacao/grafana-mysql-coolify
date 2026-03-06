# Grafana + MySql + Coolify

### Criar um usuário no mysql para exportação de métricas
```
CREATE USER 'exporter'@'%' IDENTIFIED BY 'senha_forte';
GRANT PROCESS, REPLICATION CLIENT, SELECT ON *.* TO 'exporter'@'%';
FLUSH PRIVILEGES;
```

### No grafana, criar um datasource usando o prometheus


### Add pastas/permissions para a manipulação dos volumes diretamente no server e persistir os dados dos relatórios
```
sudo chown -R 472:472 /data/grafana
sudo chmod -R 755 /data/grafana

sudo chown -R 65534:65534 /data/prometheus_data
sudo chmod -R 755 /data/prometheus_data
```

## Grafana Dashboard IDs
- MySql        = 1860
- Linux server = 7362