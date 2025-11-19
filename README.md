# Bolsa de Trabajo - Backend (completo)

Proyecto Spring Boot con MongoDB preparado para demostración.

## Requisitos
- JDK 17
- Maven
- MongoDB (localhost:27017)

## Ejecutar localmente
1. Inicia MongoDB local.
2. Desde la carpeta backend:
   - `mvn clean package`
   - `java -jar target/bolsa-trabajo-backend-0.0.1-SNAPSHOT.jar`
   - o `mvn spring-boot:run`

El proyecto incluye un `DataLoader` que crea 2 empresas y 2 ofertas si la BD está vacía.

## Endpoints principales
- POST /api/usuarios  {nombre, correo, password}
- GET /api/usuarios
- POST /api/empresas
- GET /api/empresas
- POST /api/ofertas  {titulo, descripcion, empresaId, vacantes}
- GET /api/ofertas
- GET /api/ofertas/{id}
- PUT /api/ofertas/{id}
- DELETE /api/ofertas/{id}
- POST /api/postulaciones {usuarioId, ofertaId}
- GET /api/postulaciones/usuario/{usuarioId}
- GET /api/postulaciones/oferta/{ofertaId}

Notas:
- Las contraseñas se guardan con BCrypt.
- Se incluye validación básica con `@Valid`.
