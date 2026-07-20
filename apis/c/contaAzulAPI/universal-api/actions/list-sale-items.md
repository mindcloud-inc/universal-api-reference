# Conta Azul: List Sale Items



```
GET https://connect.mindcloud.co/v1/universal/contaAzulAPI/latest/actions/list-sale-items
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Conta Azul `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/contaAzulAPI/latest/actions/list-sale-items?connectionId=$CONNECTION_ID&id_venda=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id_venda": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/contaAzulAPI/latest/actions/list-sale-items?${params}`, {
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
| `id_venda` | string | yes | Conta Azul sale identifier from the path. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "itens": [
        {}
      ],
      "itens_totais": 1,
      "totais": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `itens` | array<object> |  |
| `itens_totais` | number |  |
| `totais` | object |  |

## Native endpoint

Through the native Conta Azul API, this operation is `GET /v1/venda/{id_venda}/itens` (base URL `https://api-v2.contaazul.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-sale-items.md) for the provider-specific parameters and requirements.

