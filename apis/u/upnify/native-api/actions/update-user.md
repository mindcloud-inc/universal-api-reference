# Update User with Upnify

Updates an existing user in Upnify.

## Endpoint

- **Method:** `PUT`
- **Path:** `v4/catalogos/usuarios/:tkUsuario`
- **Base URL:** `https://api.upnify.com`
- **Official documentation:** [Update User](https://desarrollo.upnify.com/api-rest/catalogos/#api-Usuarios-PutCatalogosUsuariosTkusuario)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `tkUsuario` | path | `string` | yes | Código token que corresponde e identifica de forma única a un usuario en el sistema, al cual se requiere modificar su información.  ¿Dónde obtengo el token? |
| `nombre` | body | `string` | no | Contiene el nombre de un usuario. |
| `apellidos` | body | `string` | no | Guarda los apellidos de un usuario. |
| `iniciales` | body | `string` | no | Almacena la primera letra del nombre y apellido de un usuario. |
| `email` | body | `string` | no | Almacena el correo electrónico de un usuario. |
| `telefono` | body | `string` | no | Contiene el número de teléfono de un usuario (Si tiene un valor no númerico, devolvera un String). |
| `movil` | body | `string` | no | Guarda el número de celular de un usuario (Si tiene un valor no númerico, devolvera un String). |
| `puesto` | body | `string` | no | Define el puesto o cargo de de un usuarioen la empresa. |
| `nivel` | body | `string` | no | Código que define el nivel de privilegio de un usuario.  - 1 Administrador del sistema o Auditor.  - 2 Gerente de ventas.  - 3 Ejecutivo de ventas. |
| `tkGrupo` | body | `string` | no | Código token que corresponde a un grupo de usuarios al que pertenecerá el usuario.  ¿Dónde obtengo el token? |
| `gmt` | body | `number` | no | Guarda un código que define la zona horaria a la que pertenece un usuario.  ¿Dónde obtengo el id? |
| `pais` | body | `string` | no | Código que define el país al que pertenece el usuario.  ¿Dónde obtengo el id? |
| `estado` | body | `string` | no | Código que define un estado del país al que pertenece un usuario.  ¿Dónde obtengo el id? |
| `contrasenia1` | body | `string` | no | Almacena la contraseña establecida para el usuario. |
| `contrasenia2` | body | `string` | no | Se repite la contraseña establecida para el usuario. Este parámetro es obligatorio cuando se modifica la contraseña, se utilizan tanto los parámetros contrasenia1 y contrasenia2 |
| `comisionUsuario` | body | `string` | no | Código token que identifica de forma única a una comisión en el sistema. |
| `crearEmpresas` | body | `number` | no | Código que indica si el usuario tiene permisos para crear empresas.  - 0 No permitido.  - 1 Permitido. |
| `crearEtiquetas` | body | `number` | no | Código que indica si el usuario tiene permisos para crear etiquetas.  - 0 No permitido.  - 1 Permitido. |
| `crearPlantillas` | body | `number` | no | Código que indica si el usuario tiene permisos para crear plantillas.  - 0 No permitido.  - 1 Permitido. |
| `crearComunicaciones` | body | `number` | no | Código que indica si el usuario tiene permisos para crear comunicaciones.  - 0 No permitido.  - 1 Permitido. |
| `crearDocumentos` | body | `number` | no | Código que indica si el usuario tiene permisos para crear documentos.  - 0 No permitido.  - 1 Permitido. |
| `puedeExportar` | body | `number` | no | Código que indica si el usuario tiene permisos para exportar.  - 0 No permitido.  - 1 Permitido. |
| `hacerDescuentos` | body | `number` | no | Código que indica si el usuario tiene permisos para hacer descuentos.  - 0 No permitido.  - 1 Permitido. |
| `cambiarPrecios` | body | `number` | no | Código que indica si el usuario tiene permisos para modificar precios.  - 0 No permitido.  - 1 Permitido. |
| `mantenimientoDb` | body | `number` | no | Código que indica si el usuario tiene permisos para realizar mantenimintos a las bases de datos.  - 0 No permitido.  - 1 Permitido. |
| `etiquetar` | body | `number` | no | Código que indica si el usuario tiene permisos para realizar etiquetas.  - 0 No permitido.  - 1 Permitido. |
| `puedeCompartir` | body | `number` | no | Código que indica si el usuario tiene permisos para compartir.  - 0 No permitido.  - 1 Permitido. |
| `comisionUsuariol` | body | `number` | no | Código que indica si el usuario obtendrá algún tipo de comisión.  - 0 No permitido.  - 1 Permitido. |
| `importar` | body | `number` | no | Código que indica si el usuario tiene permisos para realizar importaciones.  - 0 No permitido.  - 1 Permitido. |
| `reasignar` | body | `number` | no | Código que indica si el usuario tiene permisos para realizar reasignaciones.  - 0 No permitido.  - 1 Permitido. |
| `facturar` | body | `number` | no | Código que indica si el usuario tiene permisos para facturar.  - 0 No permitido.  - 1 Permitido. |
| `cancelarFactura` | body | `number` | no | Código que indica si el usuario tiene permisos para cancelar facturas.  - 0 No permitido.  - 1 Permitido. |
| `verSistema` | body | `string` | no | Este código indica si el usuario tendrá permisos de administrador en el sistema, este valor es 1 cuando se desea crear un usuario de nivel "Administrador del Sistema" o "Gerente de ventas"  - 0 No es administrador.  - 1 Es administrador. |
