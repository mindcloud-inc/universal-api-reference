# Upnify: List Company Contacts

Retrieves contacts for a company in Upnify.

```
GET https://connect.mindcloud.co/v1/universal/upnify/latest/actions/list-company-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Upnify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/upnify/latest/actions/list-company-contacts?connectionId=$CONNECTION_ID&tkEmpresa=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "tkEmpresa": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/upnify/latest/actions/list-company-contacts?${params}`, {
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
| `tkEmpresa` | string | yes | Código token que identifica de forma única a una empresa en el sistema, del cual se requiere obtener los contactos asociados. ¿Dónde obtengo el token? |

## Response

```json
{
  "success": true,
  "data": [
    {
      "archivado": 1,
      "compartido": 1,
      "CompartirReasignar": 1,
      "correo": 1,
      "cp1": 1,
      "cp2": 1,
      "cp25": 1,
      "descartado": 1,
      "Descartar": 1,
      "ejecutivoNombre": "string",
      "emailConfigurado": 1,
      "empresa": "string",
      "esCliente": 1,
      "esCorreo": 1,
      "esDescartado": 1,
      "esProspecto": 1,
      "EtiquetarSeguimiento": 1,
      "etiquetas": 1,
      "fase": "string",
      "fechaContacto": "string",
      "fechaHora": "string",
      "iniciales": "string",
      "mailTo": 1,
      "movil": "string",
      "noConfigurado": 1,
      "nombreCliente": "string",
      "OportunidadArchivar": 1,
      "origen": "string",
      "puesto": "string",
      "telefono1": "string",
      "telefono2": "string",
      "tkProspecto": "string",
      "tkUsuario": "string",
      "ultimoContacto": "string",
      "ultimoContactoFechahora": "string",
      "ultimoContactoTiempo": "string",
      "ultimoUsuario": "string",
      "verArchivos": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `archivado` | number | Valor que indica si el prospecto se encuentra archivado. |
| `compartido` | number | Código que indica si el contacto ha sido compartido. |
| `CompartirReasignar` | number | Valor que indica si el usuario puede compartir un contacto reasignado. |
| `correo` | number | Indica el correo del prospecto. |
| `cp1` | number | Primer campo personalizado, que puede contener un valor perzonalido, creado por el usuario. Este campo solo será visible al seleccionarlo en la página. |
| `cp2` | number | Segundo campo personalizado, que puede contener un valor perzonalido, creado por el usuario. Este campo solo será visible al seleccionarlo en la página. |
| `cp25` | number | Vigésimo quinto campo personalizado, que puede contener un valor perzonalido, creado por el usuario. Este campo solo será visible al seleccionarlo en la página. |
| `descartado` | number | Valor que indica si el prospecto se encuentra descartado. |
| `Descartar` | number | Valor que indica si el contacto se encuentra descartado. |
| `ejecutivoNombre` | string | Contiene el nombre del ejecutivo que creó al prospecto. |
| `emailConfigurado` | number | Valor que indica si la cuenta de correo del contacto está configurada. |
| `empresa` | string | Contiene el nombre de la empresa al que está asociado el prospecto. |
| `esCliente` | number | Valor que indica si el prospecto es un cliente. |
| `esCorreo` | number | Valor tipo boleano que indica si el contacto con el prospecto es por correo. |
| `esDescartado` | number | Valor que indica si el prospecto se encuentra descartado. |
| `esProspecto` | number | Valor que indica si el prospecto aún no se ha convertido. |
| `EtiquetarSeguimiento` | number | Valor que indica si el prospecto cuenta con seguimientos. |
| `etiquetas` | number | Indica las etiquetas que la empresa tiene asociadas. |
| `fase` | string | Indica en que fase se encuentra el prospecto. |
| `fechaContacto` | string | Contiene un formato de fecha y hora que indica cuando se creó el prospecto. |
| `fechaHora` | string | Contiene un formato de fecha y hora que indica cuando se realizó la última modificación u operación con el prospecto. |
| `iniciales` | string | Contiene las iniciales del nombre del usuario que creó al prospecto. |
| `mailTo` | number | Valor que indica si se encuentra habilitado el envío de correos. |
| `movil` | string | Almacena un número de teléfono móvil de contacto del prospecto (Si tiene un valor no númerico, devolvera un String). |
| `noConfigurado` | number | Valor que indica si la cuenta del contacto está configurada. |
| `nombreCliente` | string | Almacena el nombre del prospecto. |
| `OportunidadArchivar` | number | Valor que indica si el prospecto tiene oportunidades archivadas. |
| `origen` | string | Indica desde que origen se obtuvo el prospecto. |
| `puesto` | string | Indica el puesto que ocupa el prospecto dentro de su empresa. |
| `telefono1` | string | Almacena el primer teléfono de contacto del prospecto (Si tiene un valor no númerico, devolvera un String). |
| `telefono2` | string | Almacena el segundo teléfono de contacto del prospecto (Si tiene un valor no númerico, devolvera un String). |
| `tkProspecto` | string | Código token que indifica de forma única a un prospecto en el sistema. |
| `tkUsuario` | string | Código token que identifica de forma única a un usuario. |
| `ultimoContacto` | string | Contiene una descripción de la acción realizada en el último contacto. |
| `ultimoContactoFechahora` | string | Contiene un formato de fecha y hora que indica cuando se realizó el último contacto con el prospecto. |
| `ultimoContactoTiempo` | string | Contiene un texto que indica el tiempo desde el último contacto con el prospecto. |
| `ultimoUsuario` | string | Contiene las iniciales del último usuario que tuvo contacto con el prospecto. |
| `verArchivos` | number | Código que define si el prospecto cuenta con el permiso de visualizar archivos. |

## Native endpoint

Through the native Upnify API, this operation is `GET v4/empresas/:tkEmpresa/contactos` (base URL `https://api.upnify.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-company-contacts.md) for the provider-specific parameters and requirements.

