# Conta Azul: Search Sales



```
GET https://connect.mindcloud.co/v1/universal/contaAzulAPI/latest/actions/search-sales
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Conta Azul `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/contaAzulAPI/latest/actions/search-sales?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/contaAzulAPI/latest/actions/search-sales?${params}`, {
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
      "itens": [
        {}
      ],
      "quantidades": {},
      "totais": {},
      "total_itens": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `itens` | array<object> |  |
| `quantidades` | object |  |
| `totais` | object |  |
| `total_itens` | number |  |

## Native endpoint

Through the native Conta Azul API, this operation is `GET /v1/venda/busca` (base URL `https://api-v2.contaazul.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-sales.md) for the provider-specific parameters and requirements.

