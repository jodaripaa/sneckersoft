# Documentación del Proyecto

Este documento describe los controladores, modelos y rutas del proyecto.

## Controladores

### `src/controllers/user.controller.ts`

#### Funciones:

- **`getUsers`**  
  Obtiene todos los usuarios de la base de datos.  
  **Parámetros:**  
  - `req`: Objeto de solicitud de Express.  
  - `res`: Objeto de respuesta de Express.  
  **Respuesta:**  
  - Lista de usuarios en formato JSON.  

- **`createUser`**  
  Crea un nuevo usuario en la base de datos.  
  **Parámetros:**  
  - `req`: Objeto de solicitud de Express.  
  - `res`: Objeto de respuesta de Express.  
  **Cuerpo de la solicitud:**  
  - `role`: Rol del usuario.  
  - `companyRole`: Rol en la empresa.  
  - `email`: Correo electrónico.  
  - `password`: Contraseña.  
  - `name`: Nombre del usuario.  
  - `idCard`: Documento de identidad.  
  **Respuesta:**  
  - Usuario creado en formato JSON.  

---

### `src/controllers/ticket.controller.ts`

#### Funciones:

- **`getTickets`**  
  Obtiene todos los tickets de la base de datos.  
  **Parámetros:**  
  - `req`: Objeto de solicitud de Express.  
  - `res`: Objeto de respuesta de Express.  
  **Respuesta:**  
  - Lista de tickets en formato JSON.  

- **`createTicket`**  
  Crea un nuevo ticket en la base de datos.  
  **Parámetros:**  
  - `req`: Objeto de solicitud de Express.  
  - `res`: Objeto de respuesta de Express.  
  **Cuerpo de la solicitud:**  
  - `products`: Productos incluidos en el ticket.  
  - `size`: Tamaño del ticket.  
  - `totalQuantity`: Cantidad total de productos.  
  **Respuesta:**  
  - Ticket creado en formato JSON.  

---

### `src/controllers/product.controller.ts`

#### Funciones:

- **`getProducts`**  
  Obtiene todos los productos de la base de datos.  
  **Parámetros:**  
  - `req`: Objeto de solicitud de Express.  
  - `res`: Objeto de respuesta de Express.  
  **Respuesta:**  
  - Lista de productos en formato JSON.  

- **`createProduct`**  
  Crea un nuevo producto en la base de datos.  
  **Parámetros:**  
  - `req`: Objeto de solicitud de Express.  
  - `res`: Objeto de respuesta de Express.  
  **Cuerpo de la solicitud:**  
  - `name`: Nombre del producto.  
  - `employeeCosts`: Costos de empleados asociados al producto.  
  **Respuesta:**  
  - Producto creado en formato JSON.  

---

### `src/controllers/size.controller.ts`

#### Funciones:

- **`getSizes`**  
  Obtiene todas las tallas de la base de datos.  
  **Parámetros:**  
  - `req`: Objeto de solicitud de Express.  
  - `res`: Objeto de respuesta de Express.  
  **Respuesta:**  
  - Lista de tallas en formato JSON.  

- **`createSize`**  
  Crea una nueva talla en la base de datos.  
  **Parámetros:**  
  - `req`: Objeto de solicitud de Express.  
  - `res`: Objeto de respuesta de Express.  
  **Cuerpo de la solicitud:**  
  - `productId`: ID del producto asociado.  
  - `size`: Talla del producto.  
  - `salePrice`: Precio de venta de la talla.  
  **Respuesta:**  
  - Talla creada en formato JSON.  

---

## Modelos

### `src/models/user.model.ts`

Modelo para los usuarios. Define los campos `role`, `companyRole`, `email`, `password`, `name` y `idCard`.

### `src/models/ticket.model.ts`

Modelo para los tickets. Define los campos `products`, `size` y `totalQuantity`.

### `src/models/product.model.ts`

Modelo para los productos. Define los campos `name` y `employeeCosts`.

### `src/models/size.model.ts`

Modelo para las tallas. Define los campos `productId`, `size` y `salePrice`.

---

## Rutas

### `src/routes/user.routes.ts`

Define las rutas relacionadas con los usuarios:  
- `GET /users`: Obtiene todos los usuarios.  
- `POST /users`: Crea un nuevo usuario.  

### `src/routes/ticket.routes.ts`

Define las rutas relacionadas con los tickets:  
- `GET /tickets`: Obtiene todos los tickets.  
- `POST /tickets`: Crea un nuevo ticket.  

### `src/routes/product.routes.ts`

Define las rutas relacionadas con los productos:  
- `GET /products`: Obtiene todos los productos.  
- `POST /products`: Crea un nuevo producto.  

### `src/routes/size.routes.ts`

Define las rutas relacionadas con las tallas:  
- `GET /sizes`: Obtiene todas las tallas.  
- `POST /sizes`: Crea una nueva talla.  

---

### `src/index.ts`

Archivo principal que inicializa el servidor Express.  
- **Puerto:** 3000  
- **Ruta base:**  
  - `GET /`: Responde con un mensaje indicando que el servidor está corriendo.  

Este archivo se puede expandir para incluir más detalles sobre otros controladores, modelos y rutas según sea necesario.
