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
.
├── docker-compose.yml
└── README.txt

Uso

(Ubuntu)

1.1 Instalar Docker
Seguir los pasos de la documentacion para instalar Docker
https://docs.docker.com/engine/install/ubuntu/#install-using-the-repository


1.2 Instalar Docker Compose
Seguir los pasos de la documentacion para instalar Docker Compose
https://docs.docker.com/compose/install/linux/#install-using-the-repository


1.3 Otorgar Permisos
```shell
sudo docker compose up -d

# OR
sudo usermod -aG docker $USER
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