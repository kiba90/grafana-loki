#Install
docker-compose up

#Usage
Contains:

Grafana - for graphs
Loki - for logs
Promtail - for logs delivery

http://localhosy:3000 to enter into grafana interface. Credentials are admin:admin.

For specific logs stream, you have to add to your docker-compose.yml 
```
        logging:
            driver: "json-file"
            options:
                tag: "{{.ImageName}}|{{.Name}}"
```

If you want to stream all logs from all containers, just delete in /promtail/promtail.yml this string
