Elasticsearch + Kibana con Docker Compose

Este proyecto permite levantar rápidamente un entorno de desarrollo con Elasticsearch y Kibana utilizando Docker Compose.

Requisitos
- Docker
- Docker Compose

¿Qué incluye?
- Elasticsearch 8.12.0
- Kibana 8.12.0
- Red compartida entre servicios
- Seguridad desactivada (ideal para desarrollo)

Estructura
.
├── docker-compose.yml
└── README.txt

Uso

1. Clonar el repositorio
git clone https://github.com/tu-usuario/tu-repo.git
cd tu-repo

2. Levantar los contenedores
docker-compose up -d

Esto iniciará Elasticsearch en el puerto 9200 y Kibana en el puerto 5601.

3. Verificar
- Accede a Elasticsearch: http://localhost:9200
- Accede a Kibana: http://localhost:5601

Detener los servicios
docker-compose down

Comprobación rápida (opcional)
Prueba la conexión a Elasticsearch desde terminal:
curl http://localhost:9200

Notas
- Este entorno está pensado para desarrollo. No es seguro para producción ya que desactiva la autenticación.
- Si deseas habilitar seguridad y autenticación con usuarios o API keys, se recomienda ajustar el docker-compose.yml.

Licencia
MIT