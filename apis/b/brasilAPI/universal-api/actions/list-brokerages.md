# Brasil API: List Brokerages

Retrieves CVM brokerages from Brasil API.

```
GET https://connect.mindcloud.co/v1/universal/brasilAPI/latest/actions/list-brokerages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Brasil API `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/brasilAPI/latest/actions/list-brokerages?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/brasilAPI/latest/actions/list-brokerages?${params}`, {
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
      "cnpj": "string",
      "codigo_cvm": "string",
      "email": "ava@example.com",
      "municipio": "string",
      "nome_comercial": "string",
      "nome_social": "string",
      "telefone": "string",
      "uf": "string",
      "valor_patrimonio_liquido": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cnpj` | string |  |
| `codigo_cvm` | string |  |
| `email` | string |  |
| `municipio` | string |  |
| `nome_comercial` | string |  |
| `nome_social` | string |  |
| `telefone` | string |  |
| `uf` | string |  |
| `valor_patrimonio_liquido` | string |  |

## Native endpoint

Through the native Brasil API API, this operation is `GET /cvm/corretoras/v1` (base URL `https://brasilapi.com.br/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-brokerages.md) for the provider-specific parameters and requirements.

