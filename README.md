 Inventario de Repuestos – Backend + Frontend

Aplicación full stack que permite gestionar el inventario de un almacén de repuestos. Incluye operaciones CRUD, filtrado por nombre, pruebas unitarias y frontend en Angular.

Tecnologías utilizadas

- Backend: Java 17, Spring Boot 3.5, Spring Data JPA, Maven  
- Frontend: Angular 10+  
- Base de datos: PostgreSQL  
- Pruebas: JUnit 5, Mockito, JaCoCo

 Manual de ejecución

Requisitos previos

- Java 17+
- Maven
- PostgreSQL
- Node.js + Angular CLI

Estructura del proyecto

/Repuestos/
├── backend/
├── frontend/
└── README.md

Ejecutar el backend

-bash
cd backend
mvn spring-boot:run


Por defecto corre en: `http://localhost:8080`

Ejecutar el frontend

bash
cd frontend
npm install
ng serve


Por defecto en: `http://localhost:4200`

 Script de creación de base de datos

sql
CREATE DATABASE inventario;

CREATE TABLE repuestos (
  id SERIAL PRIMARY KEY,
  nombre VARCHAR(100),
  descripcion TEXT,
  cantidad INTEGER,
  precio DOUBLE PRECISION
);

```

Puedes ejecutarlo si quieres desde una herramienta como pgAdmin, DBeaver o consola de PostgreSQL.

 Credenciales de ejemplo

Ubicadas en `backend/src/main/resources/application.properties`:

```
spring.datasource.url=jdbc:postgresql://localhost:5432/inventario
spring.datasource.username=postgres
spring.datasource.password=admin123
spring.jpa.hibernate.ddl-auto=update


Pruebas y cobertura

Para ejecutar pruebas:

bash
mvn test
```

Para generar el reporte de cobertura:

bash
mvn clean verify


El informe JaCoCo queda en:  
`backend/target/site/jacoco/index.html`


Funcionalidades destacadas

- API REST completa con operaciones CRUD
- Filtro de búsqueda por nombre de repuesto
- Arquitectura organizada por capas (`Controller`, `Service`, `Repository`, `Model`)
- Cobertura de pruebas >80 % con JaCoCo
- Interfaz Angular integrada con el backend
- Script SQL para base de datos y configuración sencilla



 Autor

Desarrollado por Linda, como parte de una prueba técnica.  
Repositorio público: [github.com/Liaav200/Repuestos](https://github.com/Liaav200/Repuestos)

