# Brasil API: Get FIPE Vehicle Prices

Retrieves FIPE vehicle prices from Brasil API by FIPE code.

```
GET https://connect.mindcloud.co/v1/universal/brasilAPI/latest/actions/get-fipe-vehicle-prices
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Brasil API `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/brasilAPI/latest/actions/get-fipe-vehicle-prices?connectionId=$CONNECTION_ID&codigoFipe=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "codigoFipe": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/brasilAPI/latest/actions/get-fipe-vehicle-prices?${params}`, {
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
| `codigoFipe` | string | yes | The FIPE code to price. |
| `tabelaReferencia` | string | no | Optional FIPE reference table code. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "anoModelo": 1,
      "codigoFipe": "string",
      "combustivel": "string",
      "dataConsulta": "string",
      "marca": "string",
      "mesReferencia": "string",
      "modelo": "string",
      "siglaCombustivel": "string",
      "tipoVeiculo": 1,
      "valor": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `anoModelo` | number |  |
| `codigoFipe` | string |  |
| `combustivel` | string |  |
| `dataConsulta` | string |  |
| `marca` | string |  |
| `mesReferencia` | string |  |
| `modelo` | string |  |
| `siglaCombustivel` | string |  |
| `tipoVeiculo` | number |  |
| `valor` | string |  |

## Native endpoint

Through the native Brasil API API, this operation is `GET /fipe/preco/v1/{codigoFipe}` (base URL `https://brasilapi.com.br/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-fipe-vehicle-prices.md) for the provider-specific parameters and requirements.

