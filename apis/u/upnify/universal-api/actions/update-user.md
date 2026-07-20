# Upnify: Update User

Updates an existing user in Upnify.

```
PUT https://connect.mindcloud.co/v1/universal/upnify/latest/actions/update-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Upnify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/upnify/latest/actions/update-user" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "tkUsuario": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/upnify/latest/actions/update-user', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "tkUsuario": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `tkUsuario` | string | yes | Código token que corresponde e identifica de forma única a un usuario en el sistema, al cual se requiere modificar su información. ¿Dónde obtengo el token? |
| `nombre` | string | no | Contiene el nombre de un usuario. |
| `apellidos` | string | no | Guarda los apellidos de un usuario. |
| `iniciales` | string | no | Almacena la primera letra del nombre y apellido de un usuario. |
| `email` | string | no | Almacena el correo electrónico de un usuario. |
| `telefono` | string | no | Contiene el número de teléfono de un usuario (Si tiene un valor no númerico, devolvera un String). |
| `movil` | string | no | Guarda el número de celular de un usuario (Si tiene un valor no númerico, devolvera un String). |
| `puesto` | string | no | Define el puesto o cargo de de un usuarioen la empresa. |
| `nivel` | string | no | Código que define el nivel de privilegio de un usuario. - 1 Administrador del sistema o Auditor. - 2 Gerente de ventas. - 3 Ejecutivo de ventas. |
| `tkGrupo` | string | no | Código token que corresponde a un grupo de usuarios al que pertenecerá el usuario. ¿Dónde obtengo el token? |
| `gmt` | number | no | Guarda un código que define la zona horaria a la que pertenece un usuario. ¿Dónde obtengo el id? |
| `pais` | string | no | Código que define el país al que pertenece el usuario. ¿Dónde obtengo el id? |
| `estado` | string | no | Código que define un estado del país al que pertenece un usuario. ¿Dónde obtengo el id? |
| `contrasenia1` | string | no | Almacena la contraseña establecida para el usuario. |
| `contrasenia2` | string | no | Se repite la contraseña establecida para el usuario. Este parámetro es obligatorio cuando se modifica la contraseña, se utilizan tanto los parámetros contrasenia1 y contrasenia2 |
| `comisionUsuario` | string | no | Código token que identifica de forma única a una comisión en el sistema. |
| `crearEmpresas` | number | no | Código que indica si el usuario tiene permisos para crear empresas. - 0 No permitido. - 1 Permitido. Default: `0`. |
| `crearEtiquetas` | number | no | Código que indica si el usuario tiene permisos para crear etiquetas. - 0 No permitido. - 1 Permitido. Default: `0`. |
| `crearPlantillas` | number | no | Código que indica si el usuario tiene permisos para crear plantillas. - 0 No permitido. - 1 Permitido. Default: `0`. |
| `crearComunicaciones` | number | no | Código que indica si el usuario tiene permisos para crear comunicaciones. - 0 No permitido. - 1 Permitido. Default: `0`. |
| `crearDocumentos` | number | no | Código que indica si el usuario tiene permisos para crear documentos. - 0 No permitido. - 1 Permitido. Default: `0`. |
| `puedeExportar` | number | no | Código que indica si el usuario tiene permisos para exportar. - 0 No permitido. - 1 Permitido. Default: `0`. |
| `hacerDescuentos` | number | no | Código que indica si el usuario tiene permisos para hacer descuentos. - 0 No permitido. - 1 Permitido. Default: `0`. |
| `cambiarPrecios` | number | no | Código que indica si el usuario tiene permisos para modificar precios. - 0 No permitido. - 1 Permitido. Default: `0`. |
| `mantenimientoDb` | number | no | Código que indica si el usuario tiene permisos para realizar mantenimintos a las bases de datos. - 0 No permitido. - 1 Permitido. Default: `0`. |
| `etiquetar` | number | no | Código que indica si el usuario tiene permisos para realizar etiquetas. - 0 No permitido. - 1 Permitido. Default: `0`. |
| `puedeCompartir` | number | no | Código que indica si el usuario tiene permisos para compartir. - 0 No permitido. - 1 Permitido. Default: `0`. |
| `comisionUsuariol` | number | no | Código que indica si el usuario obtendrá algún tipo de comisión. - 0 No permitido. - 1 Permitido. Default: `0`. |
| `importar` | number | no | Código que indica si el usuario tiene permisos para realizar importaciones. - 0 No permitido. - 1 Permitido. Default: `0`. |
| `reasignar` | number | no | Código que indica si el usuario tiene permisos para realizar reasignaciones. - 0 No permitido. - 1 Permitido. Default: `0`. |
| `facturar` | number | no | Código que indica si el usuario tiene permisos para facturar. - 0 No permitido. - 1 Permitido. Default: `0`. |
| `cancelarFactura` | number | no | Código que indica si el usuario tiene permisos para cancelar facturas. - 0 No permitido. - 1 Permitido. Default: `0`. |
| `verSistema` | string | no | Este código indica si el usuario tendrá permisos de administrador en el sistema, este valor es 1 cuando se desea crear un usuario de nivel "Administrador del Sistema" o "Gerente de ventas" - 0 No es administrador. - 1 Es administrador. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": 1,
      "msg": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | number | Proporciona un código de verificación como respuesta. |
| `msg` | string | Proporciona un mensaje descriptivo o razón dependiendo el resultado.  - 0 Proceso correcto. - 1 Falló la inserción. - 2 Faltan parámetros. - 3 Error al eliminar el registro. - 4 Token de sesión vencido.  - 5 Fallo de procedimiento en base de datos. - 6 Permisos insuficientes. - 7 Mensajes en la lógica de negocios. |

## Native endpoint

Through the native Upnify API, this operation is `PUT v4/catalogos/usuarios/:tkUsuario` (base URL `https://api.upnify.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-user.md) for the provider-specific parameters and requirements.

