# Nombre del Proyecto

## Descripción

## Instalación
### 1. Clonar el repositorio

```bash
git clone https://github.com/usuario/orquicombeima.git
```

### 2. Ingresar a la carpeta del proyecto

```bash
cd orquicombeima
```

### 3. Configurar la base de datos

Crear una base de datos en MySQL llamada:

```sql
CREATE DATABASE orquicombeima;
```

Configurar el archivo:

`src/main/resources/application.properties`

Con tus credenciales:

```properties
spring.datasource.url=jdbc:mysql://localhost:3306/orquicombeima
spring.datasource.username=root
spring.datasource.password=tu_contraseña
```

### 4. Instalar dependencias

```bash
mvn clean install
```

### 5. Ejecutar el proyecto

```bash
mvn spring-boot:run
```

---

## Uso

Una vez iniciado, abrir en el navegador:

```bash
http://localhost:8080
```

### Ejemplo de uso

1. Registrarse como usuario
2. Iniciar sesión
3. Explorar el catálogo de orquídeas
4. Agregar productos al carrito
5. Confirmar pedido
6. Recibir resumen automático por WhatsApp

### Probar endpoints

Consultar productos:

```http
GET http://localhost:8080/api/productos
```

Crear pedido:

```http
POST http://localhost:8080/api/pedidos
```

---

## Autores

- Juan Sebastian Gallego Villamil
- Steven

---

## Flujo de trabajo Git
Para el desarrollo del proyecto se siguió una estrategia basada en **Git Flow**, utilizando diferentes ramas para organizar el trabajo colaborativo.

### Rama `develop`

La rama `develop` fue utilizada como rama principal de integración durante el desarrollo.

En esta rama se consolidaron todas las funcionalidades desarrolladas en ramas feature antes de pasar a producción.

Ejemplo:

```bash
git checkout develop
git merge feature/autenticacion
git merge feature/carrito-compras
```

---

### Ramas `feature/`

Cada nueva funcionalidad fue desarrollada en una rama independiente.

Ejemplos de ramas utilizadas:

- `feature/login`
- `feature/catalogo-orquideas`
- `feature/carrito-compras`
- `feature/integracion-whatsapp`

Creación de una rama feature:

```bash
git checkout -b feature/nueva-funcionalidad
```

Una vez terminada:

```bash
git checkout develop
git merge feature/nueva-funcionalidad
```

---

### Rama `release/v1.0.0`

Cuando el sistema alcanzó una versión estable, se creó la rama:

```bash
release/v1.0.0
```

Esta rama se utilizó para:

- Realizar pruebas finales
- Corregir errores menores
- Ajustar documentación
- Preparar la versión final

Creación:

```bash
git checkout -b release/v1.0.0
```

Posteriormente se integró a `main`.

---

### Rama `hotfix/readme-typo`

Después de liberar la versión final, se detectó un error menor en la documentación del README.

Para solucionarlo se creó:

```bash
hotfix/readme-typo
```

Esta rama permitió corregir rápidamente el error sin afectar el desarrollo principal.

Ejemplo:

```bash
git checkout -b hotfix/readme-typo
git commit -m "Corrección de error tipográfico en README"
```

---

### Tag final `v1.0.0`

La versión final del proyecto fue marcada con el tag:

```bash
v1.0.0
```

Creación del tag:

```bash
git tag -a v1.0.0 -m "Versión estable final"
git push origin v1.0.0
```

Este tag representa la primera versión estable y funcional del sistema.

---

### Flujo general utilizado

```text
main
 └── develop
      ├── feature/login
      ├── feature/catalogo
      ├── feature/carrito
      ├── release/v1.0.0
      └── hotfix/readme-typo
```

## Evidencias
### Capturas del sistema

- Pantalla de inicio
- Catálogo de productos
- Carrito de compras
- Confirmación de pedido