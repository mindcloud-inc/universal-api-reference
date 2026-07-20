# Upnify: Get User

Retrieves a user from Upnify.

```
GET https://connect.mindcloud.co/v1/universal/upnify/latest/actions/get-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Upnify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/upnify/latest/actions/get-user?connectionId=$CONNECTION_ID&tkUsuario=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "tkUsuario": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/upnify/latest/actions/get-user?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `tkUsuario` | string | yes | Código token que corresponde e identifica de forma única a un usuario en el sistema, del cual se requiere obtener los detalles. ¿Dónde obtengo el token? |

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
      "etiquetar": 1,
      "fuerzaContrasenia": "string",
      "gmt": 1,
      "grupo": "string",
      "gruposAccesos": {},
      "gruposInteracciones": {},
      "hacerDescuentos": 1,
      "idestado": "string",
      "idioma": 1,
      "idnivel": "string",
      "idpais": "string",
      "iniciales": "string",
      "integrante": "string",
      "mantenimientoDb": 1,
      "movil": "string",
      "nombre": "string",
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
      "tkUsuario": "string",
      "usuariosAccesos": {},
      "usuariosInteracciones": {}
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
| `crearComunicaciones` | number | Código que indica si el usuario tiene permisos para crear comunicaciones.  - 0 No permitido.  - 1 Solo uso.  - 2 Uso y creación. |
| `crearDocumentos` | number | Código que indica si el usuario tiene permisos para crear documentos.  - 0 No permitido.  - 1 Solo uso.  - 2 Uso y creación. |
| `crearEmpresas` | number | Código que indica si el usuario tiene permisos para crear empresas.  - 0 Solo uso.  - 1 Uso y creación. |
| `crearEtiquetas` | number | Código que indica si el usuario tiene permisos para crear etiquetas.  - 0 No permitido.  - 1 Crear y eliminar. |
| `crearPlantillas` | number | Código que indica si el usuario tiene permisos para crear plantillas.  - 0 No permitido.  - 1 Solo uso.  - 2 Uso y creación. |
| `email` | string | Almacena el correo electrónico de un usuario. |
| `etiquetar` | number | Código que indica si el usuario tiene permisos para realizar etiquetas.  - 0 No permitido.  - 1 Agregar etiquetas.  - 2 Quitar etiquetas.  - 3 Agregar o quitar etiquetas.. |
| `fuerzaContrasenia` | string | Almacena un código que define si una contraseña de usuario es segura. |
| `gmt` | number | Guarda un código que define la zona horaria a la que pertenece un usuario. |
| `grupo` | string | Contiene el grupo al que fue asignado un usuario. |
| `gruposAccesos` | object | Almacena a los grupos con los que tiene permiso de ver información. |
| `gruposInteracciones` | object | Almacena a los grupos con los que puede interactuar. |
| `hacerDescuentos` | number | Código que indica si el usuario tiene permisos para hacer descuentos.  - 0 No permitido.  - 1 Solo uso.  - 2 Uso y creación. |
| `idestado` | string | Código que define un estado del país al que pertenece un usuario. |
| `idioma` | number | Almacena el idioma preferente del usuario . |
| `idnivel` | string | Código que define el nivel de privilegio de un usuario . |
| `idpais` | string | Código que define el país al que pertenece el usuario. |
| `iniciales` | string | Almacena la primera letra del nombre y apellido de un usuario. |
| `integrante` | string | Variable que almacena el apellido y nombre de un usuario. |
| `mantenimientoDb` | number | Código que indica si el usuario tiene permisos para realizar mantenimintos a las bases de datos.  - 0 No permitido.  - 1 Combinar registros.  - 2 Combinar y mostrar inconsistencias. |
| `movil` | string | Guarda el número de celular de un usuario (Si tiene un valor no númerico, devolvera un String). |
| `nombre` | string | Contiene el nombre de un usuario. |
| `puedeCancelarFactura` | number | Código que define si el usuario tiene permiso de cancelar la factura .  - 0 No permitido.  - 1 Permitido. |
| `puedeCompartir` | number | Código que indica si el ejecutivo de la sesion tiene permitido compartir el cliente.  - 0 No permitido.  - 1 Solo descompartir.  - 2 Solo compartir.  - 3 Compartir y descompartir. |
| `puedeExportar` | number | Código que define si el usuario tiene permiso para exportar. |
| `puedeFacturar` | number | Indica si el ejecutivo que atendió la venta puede facturar.  - 0 No puede facturar.  - 1 Puede Facturar. |
| `puedeImportar` | number | Código que define si el usuario tiene permiso para importar.  - 0 No permitido.  - 1 Permitido. |
| `puedeReasignar` | number | Código que indica si el ejecutivo de la sesion tiene permitido reasignar el prospecto.  - 0 No permitido.  - 1 Permitido. |
| `puesto` | string | Define el puesto o cargo de de un usuarioen la empresa. |
| `telefono` | string | Contiene el número de teléfono de un usuario (Si tiene un valor no númerico, devolvera un String). |
| `tituloNivel` | string | Almacena el nombre del nivel de privilegios seleccionado durante la creación del usuario. |
| `tkGrupo` | string | Código token que corresponde a un grupo. |
| `tkUsuario` | string | Guarda un código token que corresponde a un usuario del sistema. |
| `usuariosAccesos` | object | Almacena los usuarios con los que tiene permiso de ver información. |
| `usuariosInteracciones` | object | Almacena a los usuarios con los que puede interactuar. |

## Native endpoint

Through the native Upnify API, this operation is `GET v4/catalogos/usuarios/:tkUsuario` (base URL `https://api.upnify.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-user.md) for the provider-specific parameters and requirements.

