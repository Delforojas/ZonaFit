# ZonaFit
Aplicación de consola en Python para la gestión de clientes de un gimnasio. Permite listar, agregar, modificar y eliminar registros de clientes desde una base de datos MySQL utilizando conexión mediante pool.

📁 Estructura del Proyecto
zona_fit_db/
│
├── cliente.py           # Clase Cliente (modelo)
├── cliente_dao.py       # Acceso a datos (DAO)
├── conexion.py          # Gestión de conexión MySQL con pool
├── zona_fit_app.py      # Aplicación principal con menú interactivo
└── README.md            # (Este archivo)

🔧 Tecnologías utilizadas
Python 3.13
MySQL Connector (mysql-connector-python)
MySQL Server
Programación orientada a objetos (OOP)
Patrón DAO (Data Access Object)

🧱 Clases del proyecto
Cliente
Contiene los atributos de un cliente:
-id
-nombre
-apellido
-membresia

ClienteDAO
Se encarga de las operaciones con la base de datos:
-seleccionar() - Lista todos los clientes.
-insertar(cliente) - Inserta un nuevo cliente.
-actualizar(cliente) - Modifica un cliente existente.
-eliminar(cliente) - Elimina un cliente por ID.

Conexion
Maneja la conexión a la base de datos mediante pool:
-obtener_pool() - Crea o reutiliza un pool de conexiones.
-obtener_conexion() - Obtiene una conexión desde el pool.
-liberar_conexion(conexion) - Cierra la conexión.

zona_fit_app.py
Archivo principal que presenta un menú para el usuario con las siguientes opciones:
-Listar clientes
-Agregar cliente
-Modificar cliente
-Eliminar cliente

Salir
