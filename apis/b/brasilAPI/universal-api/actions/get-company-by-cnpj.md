# Brasil API: Get Company by CNPJ

Retrieves company details from Brasil API by CNPJ.

```
GET https://connect.mindcloud.co/v1/universal/brasilAPI/latest/actions/get-company-by-cnpj
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Brasil API `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/brasilAPI/latest/actions/get-company-by-cnpj?connectionId=$CONNECTION_ID&cnpj=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "cnpj": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/brasilAPI/latest/actions/get-company-by-cnpj?${params}`, {
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
| `cnpj` | string | yes | The 14-digit CNPJ identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "bairro": "string",
      "capital_social": 1,
      "cep": 1,
      "cnaes_secundarios": [
        {}
      ],
      "cnpj": "string",
      "complemento": "string",
      "descricao_situacao_cadastral": "string",
      "email": "ava@example.com",
      "logradouro": "string",
      "municipio": "string",
      "nome_fantasia": "string",
      "numero": "string",
      "qsa": [
        {}
      ],
      "razao_social": "string",
      "regime_tributario": [
        {}
      ],
      "situacao_cadastral": 1,
      "uf": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `bairro` | string |  |
| `capital_social` | number |  |
| `cep` | number |  |
| `cnaes_secundarios` | array<object> |  |
| `cnpj` | string |  |
| `complemento` | string |  |
| `descricao_situacao_cadastral` | string |  |
| `email` | string |  |
| `logradouro` | string |  |
| `municipio` | string |  |
| `nome_fantasia` | string |  |
| `numero` | string |  |
| `qsa` | array<object> |  |
| `razao_social` | string |  |
| `regime_tributario` | array<object> |  |
| `situacao_cadastral` | number |  |
| `uf` | string |  |

## Native endpoint

Through the native Brasil API API, this operation is `GET /cnpj/v1/{cnpj}` (base URL `https://brasilapi.com.br/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-company-by-cnpj.md) for the provider-specific parameters and requirements.

