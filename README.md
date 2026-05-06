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

## Evidencias
### Capturas del sistema

- Pantalla de inicio
- Catálogo de productos
- Carrito de compras
- Confirmación de pedido