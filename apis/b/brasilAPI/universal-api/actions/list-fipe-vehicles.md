# Brasil API: List FIPE Vehicles

Retrieves FIPE vehicles from Brasil API by brand and vehicle type.

```
GET https://connect.mindcloud.co/v1/universal/brasilAPI/latest/actions/list-fipe-vehicles
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Brasil API `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/brasilAPI/latest/actions/list-fipe-vehicles?connectionId=$CONNECTION_ID&tipoVeiculo=string&codigoMarca=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "tipoVeiculo": "string",
  "codigoMarca": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/brasilAPI/latest/actions/list-fipe-vehicles?${params}`, {
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
| `tipoVeiculo` | string | yes | The FIPE vehicle type. |
| `codigoMarca` | string | yes | The FIPE brand code. |
| `tabelaReferencia` | string | no | Optional FIPE reference table code. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "modelo": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `modelo` | string |  |

## Native endpoint

Through the native Brasil API API, this operation is `GET /fipe/veiculos/v1/{tipoVeiculo}/{codigoMarca}` (base URL `https://brasilapi.com.br/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-fipe-vehicles.md) for the provider-specific parameters and requirements.

