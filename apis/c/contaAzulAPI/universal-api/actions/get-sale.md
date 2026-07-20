# Conta Azul: Get Sale



```
GET https://connect.mindcloud.co/v1/universal/contaAzulAPI/latest/actions/get-sale
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Conta Azul `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/contaAzulAPI/latest/actions/get-sale?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/contaAzulAPI/latest/actions/get-sale?${params}`, {
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
| `id` | string | yes | Conta Azul sale identifier from the path. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "cliente": {},
      "contrato": {},
      "evento_financeiro": {},
      "venda": {},
      "vendedor": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cliente` | object |  |
| `contrato` | object |  |
| `evento_financeiro` | object |  |
| `venda` | object |  |
| `vendedor` | object |  |

## Native endpoint

Through the native Conta Azul API, this operation is `GET /v1/venda/{id}` (base URL `https://api-v2.contaazul.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-sale.md) for the provider-specific parameters and requirements.

