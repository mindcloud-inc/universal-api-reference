# Brasil API: Get Brokerage by CNPJ

Retrieves a brokerage from Brasil API by CNPJ.

```
GET https://connect.mindcloud.co/v1/universal/brasilAPI/latest/actions/get-brokerage-by-cnpj
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Brasil API `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/brasilAPI/latest/actions/get-brokerage-by-cnpj?connectionId=$CONNECTION_ID&cnpj=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "cnpj": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/brasilAPI/latest/actions/get-brokerage-by-cnpj?${params}`, {
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
| `cnpj` | string | yes | The brokerage CNPJ identifier. |

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

Through the native Brasil API API, this operation is `GET /cvm/corretoras/v1/{cnpj}` (base URL `https://brasilapi.com.br/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-brokerage-by-cnpj.md) for the provider-specific parameters and requirements.

