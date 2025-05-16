Sprint3 Linux
Este proyecto demuestra cómo ejecutar una aplicación Spring Boot que se conecta a una base de datos Oracle usando Docker Compose.

📋 Contenido:
-Tecnologías
-Prerrequisitos
-Instalación y ejecución
-Verificación
-Estructura del proyecto

🔧 Tecnologías utilizadas:
Java 17
Spring Boot 
Oracle Database 
Docker
Docker Compose
Maven

🚀 Instalación y ejecución
✅ Prerrequisitos
Antes de comenzar, asegúrate de tener instalado en tu máquina:

Docker
Docker Compose
Java 17
Maven (mvn) o usar el wrapper incluido (./mvnw)

🧪 Pasos para ejecutar el proyecto

1.Clonar el repositorio:
bashgit clone https://github.com/CarlosSanchezL/Sprint3-Linux.git
cd spring-linux-project

2.Compilar el proyecto:
bash./mvnw clean package

3.Levantar los contenedores con Docker Compose:
bashdocker-compose up --build
Para ejecutar en modo desacoplado (background):
bashdocker-compose up --build -d


4.Verificación
Abre tu navegador y navega a:
http://localhost:8080
Deberías ver el mensaje:

Spring Boot + Oracle XE corriendo correctamente!

5.Estructura del proyecto
spring-linux-project/
├── src/                    # Código fuente de la aplicación
├── Dockerfile              # Configuración para crear la imagen Docker de la aplicación
├── docker-compose.yml      # Configuración de los servicios (app + base de datos)
├── pom.xml                 # Dependencias y configuración de Maven
└── README.md               # Este archivo
6.Detener la aplicación
Para detener los contenedores:
bashdocker-compose down
Para eliminar los volúmenes también:
bashdocker-compose down -v