# Grafana + MySql + Coolify

### Criar um usuário no mysql para exportação de métricas
```
CREATE USER 'exporter'@'%' IDENTIFIED BY 'senha_forte';
GRANT PROCESS, REPLICATION CLIENT, SELECT ON *.* TO 'exporter'@'%';
FLUSH PRIVILEGES;
```

### No grafana, criar um datasource usando o prometheus
