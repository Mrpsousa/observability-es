## observability-es

### Antes de executar o docker-compose up, crie a rede observability com o comando
    $ docker network create observability

### Também é necessário criar a pasta elasticsearch_data no fc2-observabilidade-elastic na máquina local manualmente para evitar erro de permissionamento
    $ mkdir elasticsearch_data

### Na pasta /beats/metric execute o seguinte comando:
    $ sudo chown root metricbeat.yml 

### Caso ocorra o erro 
    bootstrap check failure [1] of [1]: max virtual memory areas vm.max_map_count [65530] is too low, increase to at least [262144]

### Execute o comando 
    sysctl -w vm.max_map_count=262144