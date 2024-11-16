# backInstrucciones para Backend (Spring Boot)
Requisitos previos
Tener Java 11 o superior instalado.
Tener Maven instalado.
1. Clonar el Repositorio del Backend
Si aún no has clonado el proyecto:
git clone <URL_DEL_REPOSITORIO_BACKEND>
cd <nombre_del_directorio_del_backend>
2. Instalación de Dependencias
Maven se encargará de instalar todas las dependencias necesarias para el proyecto. Abre una terminal en el directorio del proyecto y ejecuta:

bash
Copiar código
mvn install
3. Configuración del Archivo application.properties
Dirígete al archivo src/main/resources/application.properties y configura las siguientes propiedades:

properties
Copiar código
# Configuración de la base de datos
spring.datasource.url=jdbc:mysql://localhost:3306/tipo_cambio_db
spring.datasource.username=root
spring.datasource.password=your_password
spring.jpa.hibernate.ddl-auto=update

# URL del servicio SOAP
soap.wsdl.url=https://www.banguat.gob.gt/variables/ws/TipoCambio.asmx?WSDL

# Otras configuraciones
server.port=8080
Asegúrate de que la base de datos esté configurada correctamente y de que el servicio SOAP del Banco de Guatemala sea accesible.

4. Ejecutar el Backend
Para ejecutar el backend, utiliza el siguiente comando:

bash
Copiar código
mvn spring-boot:run
El servidor backend se ejecutará en http://localhost:8080, y podrás acceder a la API REST para obtener el tipo de cambio.
