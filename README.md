# LaberintoLibros_2023
# Proyecto-Grupo1

## Usuarios y Contraseñas

- **Usuario Administrador**:
    - Usuario: `Admin`
    - Contraseña: `Admin`

- **Usuario Consulta**:
    - Usuario: `Consulta`
    - Contraseña: `Consulta`

- **Usuario Cliente**:
    - Usuario: `Cliente`
    - Contraseña: `Cliente`

## Creación de las carpetas y rutas para los archivos serializables

Para garantizar el funcionamiento correcto del proyecto, es necesario crear ciertas carpetas y asegurarse de que los archivos correctos estén en el lugar adecuado. A continuación te explico cómo hacerlo:

### 1. Crear las carpetas

Al descomprimir o clonar el proyecto, deberás crear una carpeta llamada **"Archivos"** en la raíz del proyecto.  
Dentro de la carpeta **"Archivos"**, debes crear otras tres carpetas con los siguientes nombres:

- **Carpeta1**
- **Carpeta2**
- **Carpeta3**

### 2. Añadir archivos

Dentro de **cualquiera de las carpetas mencionadas** (Carpeta1, Carpeta2, Carpeta3), debes copiar y pegar los archivos **.txt** que se usan para manejar los datos con **JSON**.  
Esto es esencial para que el sistema funcione correctamente, ya que el código está utilizando rutas absolutas en vez de relativas para acceder a estos archivos.

### 3. Modificar rutas en el código

- Ve al archivo **Json_Utility**.
- En el método `createPathFather()`, cambia la ruta de los archivos en la primera línea para que apunte a la ubicación donde has colocado las carpetas **Archivos** y las subcarpetas (**Carpeta1**, **Carpeta2**, **Carpeta3**).
- En el mismo archivo, dentro del método `getPath()`, localiza el último `if` y cambia la ruta por la misma que has puesto antes, pero añadiendo `\\Carpeta2` al final de la ruta.

## Uso de Librerías

Asegúrate de agregar las siguientes librerías a tu proyecto:

- **Librerías dentro de WinRar.lib**.
- **Dependencia `com.itextpdf.text`**.

### Posibles Errores

Si encuentras un error relacionado con el correo electrónico, sigue estos pasos:

1. Dirígete al archivo **module-info.java**.
2. Comenta la línea que dice `// requires javax.mail.api;`.

### Ingreso de Nuevo Cliente

Para registrar un nuevo cliente, es importante que el correo ingresado sea **real** y esté **bien escrito**. El correo debe cumplir con estos requisitos:

- Debe incluir el símbolo **@**.
- Debe terminar con **.com**.
- El dominio debe ser real y válido.
