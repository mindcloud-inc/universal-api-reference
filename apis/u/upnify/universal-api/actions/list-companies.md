# Upnify: List Companies

Retrieves companies from Upnify.

```
GET https://connect.mindcloud.co/v1/universal/upnify/latest/actions/list-companies
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Upnify `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/upnify/latest/actions/list-companies?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/upnify/latest/actions/list-companies?${params}`, {
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
      "companiaGrupo": "string",
      "empresa": "string",
      "fechaCreacion": "2026-05-07T12:00:00.000Z",
      "idExterno": 1,
      "indice": 1,
      "industria": "string",
      "telefonoCorporativo": "string",
      "tkCompaniaGrupo": "string",
      "tkEmpresa": "string",
      "tkIndustria": "string",
      "tkUsuario": "string",
      "ultimaModificacion": "string",
      "url": "https://example.com",
      "usuario": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `companiaGrupo` | string | Contiene el grupo al que pertenece la empresa en caso de pertenecer a alguno. |
| `empresa` | string | Contiene el nombre de la empresa. |
| `fechaCreacion` | date | Contiene la fecha de creación de la empresa. |
| `idExterno` | number | Codigo utilizado para identificar a la empresa desde fuera del sistema. |
| `indice` | number | Define la posición del registro respecto a los demás registros. |
| `industria` | string | Especifica a que tipo de insdustria pertenece la empresa. |
| `telefonoCorporativo` | string | Guarda el número de telefono de la empresa (Si tiene un valor no númerico, devolvera un String). |
| `tkCompaniaGrupo` | string | Código token que identifica de forma única a un grupo para empresas. |
| `tkEmpresa` | string | Código token que identifica de forma única a una empresa en el sistema. |
| `tkIndustria` | string | Código token que identifica de forma única a una industria. |
| `tkUsuario` | string | Código token que identifica de forma única a un usuario en el sistema. |
| `ultimaModificacion` | string | Contiene un formato compuesto de fecha y hora que indica cuando fué la última modificación de la enmpresa. |
| `url` | string | Guarda la dirección del sitio web de la empresa. |
| `usuario` | string | Contiene el nombre del usuario de la compania. |

## Native endpoint

Through the native Upnify API, this operation is `GET v4/empresas` (base URL `https://api.upnify.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-companies.md) for the provider-specific parameters and requirements.

