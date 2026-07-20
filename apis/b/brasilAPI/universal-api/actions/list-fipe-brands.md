# Brasil API: List FIPE Brands

Retrieves FIPE brands from Brasil API by vehicle type.

```
GET https://connect.mindcloud.co/v1/universal/brasilAPI/latest/actions/list-fipe-brands
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Brasil API `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/brasilAPI/latest/actions/list-fipe-brands?connectionId=$CONNECTION_ID&tipoVeiculo=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "tipoVeiculo": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/brasilAPI/latest/actions/list-fipe-brands?${params}`, {
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
| `tabelaReferencia` | string | no | Optional FIPE reference table code. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "nome": "string",
      "valor": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `nome` | string |  |
| `valor` | number |  |

## Native endpoint

Through the native Brasil API API, this operation is `GET /fipe/marcas/v1/{tipoVeiculo}` (base URL `https://brasilapi.com.br/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-fipe-brands.md) for the provider-specific parameters and requirements.

