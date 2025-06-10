Elasticsearch + Kibana con Docker Compose

Este proyecto permite levantar rápidamente un entorno de desarrollo con Elasticsearch y Kibana utilizando Docker Compose.

Requisitos
- Docker
- Docker Compose

¿Qué incluye?
- Elasticsearch 9.0.0
- Kibana 9.0.0
- Red compartida entre servicios
- Seguridad desactivada (ideal para desarrollo)
- Docker
- Docker Compose

Estructura
├── docker-compose.yml
└── README.txt

Uso

(Ubuntu)

1 Actualizar dependencias
```
sudo apt update && sudo apt upgrade -y
```

1.1 Instalar Docker
Seguir los pasos de la documentacion para instalar Docker
https://docs.docker.com/engine/install/ubuntu/#install-using-the-repository


1.2 Instalar Docker Compose
Seguir los pasos de la documentacion para instalar Docker Compose
https://docs.docker.com/compose/install/linux/#install-using-the-repository


2 Politicas y permisos

2.1 Crear el grupo
```
sudo groupadd elasticgroup
```

2.2 Crear un usuario de administración (opcional)
```
sudo adduser elasticadmin
```

2.3 Agregar el usuario al grupo personalizado

```
sudo usermod -aG elasticgroup elasticadmin
```

2.4 Dar permisos de Docker a ese grupo
```
sudo chgrp elasticgroup /var/run/docker.sock
sudo chmod 660 /var/run/docker.sock
```

2.1 Clonar el repositorio
```shell
git clone https://github.com/tu-usuario/tu-repo.git
cd tu-repo
```

3.1 Levantar los servicios
```shell
docker-compose up -d
```

3.2 Verifica que los contenedores estén activos:
```bash
docker ps
```

3.3 Validar logs de Kibana/ElasticSearch
```shell
docker logs -f <NOMBRE_INSTANCIA>
```

3.4 Apagar instancias de Docker
```
docker compose down -v
```