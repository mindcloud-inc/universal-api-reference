# Upnify: List Users

Retrieves users from Upnify.

```
GET https://connect.mindcloud.co/v1/universal/upnify/latest/actions/list-users
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Upnify `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/upnify/latest/actions/list-users?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/upnify/latest/actions/list-users?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "activo": 1,
      "apellidos": "string",
      "avatar": "string",
      "cambiarPrecios": 1,
      "correoConfigurado": 1,
      "crearComunicaciones": 1,
      "crearDocumentos": 1,
      "crearEmpresas": 1,
      "crearEtiquetas": 1,
      "crearPlantillas": 1,
      "email": "ava@example.com",
      "estado": "string",
      "etiquetar": 1,
      "fuerzaContrasenia": "string",
      "gmt": 1,
      "grupo": "string",
      "hacerDescuentos": 1,
      "idioma": 1,
      "indice": 1,
      "iniciales": "string",
      "integrante": "string",
      "mantenimientoDb": 1,
      "movil": "string",
      "nivel": 1,
      "nombre": "string",
      "pais": "string",
      "puedeCancelarFactura": 1,
      "puedeCompartir": 1,
      "puedeExportar": 1,
      "puedeFacturar": 1,
      "puedeImportar": 1,
      "puedeReasignar": 1,
      "puesto": "string",
      "telefono": "string",
      "tituloNivel": "string",
      "tkGrupo": "string",
      "tkUsuario": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `activo` | number | Determina si un usuario se encuentra activo o no en el sistema. |
| `apellidos` | string | Guarda los apellidos de un usuario. |
| `avatar` | string | Contiene la imagen que el usuario haya seleccionado como su avatar, la imagen está codificada en base64. |
| `cambiarPrecios` | number | Código que indica si el usuario tiene permisos para modificar precios.  - 0 No permitido.  - 1 Permitido. |
| `correoConfigurado` | number | Código que define si el usuario configurado su correo o no .  - 0 No configurado.  - 1 Configurado. |
| `crearComunicaciones` | number | Código que indica si el usuario tiene permisos para crear comunicaciones.  - 0 No permitido.  - 1 Permitido. |
| `crearDocumentos` | number | Código que indica si el usuario tiene permisos para crear documentos.  - 0 No permitido.  - 1 Permitido. |
| `crearEmpresas` | number | Código que indica si el usuario tiene permisos para crear empresas.  - 0 No permitido.  - 1 Permitido. |
| `crearEtiquetas` | number | Código que indica si el usuario tiene permisos para crear etiquetas.  - 0 No permitido.  - 1 Permitido. |
| `crearPlantillas` | number | Código que indica si el usuario tiene permisos para crear plantillas.  - 0 No permitido.  - 1 Permitido. |
| `email` | string | Almacena el correo electrónico de un usuario. |
| `estado` | string | Código que define un estado del país al que pertenece un usuario. |
| `etiquetar` | number | Código que indica si el usuario tiene permisos para realizar etiquetas.  - 0 No permitido.  - 1 Permitido. |
| `fuerzaContrasenia` | string | Almacena un código que define si una contraseña de usuario es segura. |
| `gmt` | number | Guarda un código que define la zona horaria a la que pertenece un usuario. |
| `grupo` | string | Contiene el grupo al que fue asignado un usuario. |
| `hacerDescuentos` | number | Código que indica si el usuario tiene permisos para hacer descuentos.  - 0 No permitido.  - 1 Permitido. |
| `idioma` | number | Almacena el idioma preferente del usuario . |
| `indice` | number | Define la posición de un registro, con respecto a los demás registros. |
| `iniciales` | string | Almacena la primera letra del nombre y apellido de un usuario. |
| `integrante` | string | Variable que almacena el apellido y nombre de un usuario. |
| `mantenimientoDb` | number | Código que indica si el usuario tiene permisos para realizar mantenimintos a las bases de datos.  - 0 No permitido.  - 1 Permitido. |
| `movil` | string | Guarda el número de celular de un usuario (Si tiene un valor no númerico, devolvera un String). |
| `nivel` | number | Código que define el nivel de privilegio de un usuario . |
| `nombre` | string | Contiene el nombre de un usuario. |
| `pais` | string | Código que define el país al que pertenece el usuario. |
| `puedeCancelarFactura` | number | Código que define si el usuario tiene permiso de cancelar la factura .  - 0 No permitido.  - 1 Permitido. |
| `puedeCompartir` | number | Código que indica si el ejecutivo de la sesion tiene permitido compartir el cliente.  - 0 No permitido.  - 1 Permitido. |
| `puedeExportar` | number | Código que define si el usuario tiene permiso para exportar. |
| `puedeFacturar` | number | Indica si el ejecutivo que atendió la venta puede facturar.  - 0 No puede facturar.  - 1 Puede Facturar. |
| `puedeImportar` | number | Código que define si el usuario tiene permiso para importar.  - 0 No permitido.  - 1 Permitido. |
| `puedeReasignar` | number | Código que indica si el ejecutivo de la sesion tiene permitido reasignar el cliente.  - 0 No permitido.  - 1 Permitido. |
| `puesto` | string | Define el puesto o cargo de de un usuario en la empresa. |
| `telefono` | string | Contiene el número de teléfono de un usuario (Si tiene un valor no númerico, devolvera un String). |
| `tituloNivel` | string | Almacena el nombre del nivel de privilegios seleccionado durante la creación del usuario. |
| `tkGrupo` | string | Código token que corresponde a un grupo. |
| `tkUsuario` | string | Guarda un código token que corresponde a un usuario del sistema. |

## Native endpoint

Through the native Upnify API, this operation is `GET v4/catalogos/usuarios` (base URL `https://api.upnify.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-users.md) for the provider-specific parameters and requirements.

