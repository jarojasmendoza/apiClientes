# API REST de Gestión de Usuarios

Esta API REST proporciona endpoints para la gestión de usuarios, incluyendo la creación, consulta y modificación de usuarios.

## Requisitos previos

- Java JDK 8 o superior
- Gradle 8.0 o superior
- IDE de desarrollo compatible con Java (por ejemplo, IntelliJ IDEA, Eclipse)
- Postman u otra herramienta similar para probar las solicitudes HTTP

## Ejecución del proyecto

1. Clona el repositorio desde GitHub: 
git clone https://github.com/jarojasmendoza/apiClientes.git
2. Abre el proyecto en tu IDE de desarrollo.
3. Ejecuta la aplicación desde tu IDE o utilizando Gradle:
4. La API estará disponible en `http://localhost:8080`.
## Endpoints disponibles

### Crear usuario

- **URL:** `POST /api/usuarios/crear`
- **Descripción:** Crea un nuevo usuario con los datos proporcionados.
- **Cuerpo de la solicitud:**
```json
{
 "name": "Juan Rodriguez",
 "email": "juan@rodriguez.org",
 "password": "hunter2J@1as",
 "phones": [
   {
     "number": "123456789",
     "citycode": "1",
     "contrycode": "57"
   }
 ]
}
```

#### Respuesta exitosa:

Código de estado: 201 (Created)
Cuerpo de la respuesta: Usuario creado con éxito, incluyendo ID, fecha de creación, fecha de modificación, último inicio de sesión, token y estado de activación.
#### Errores posibles:

Código de estado: 400 (Bad Request)
Cuerpo de la respuesta: Mensaje de error indicando el problema encontrado.