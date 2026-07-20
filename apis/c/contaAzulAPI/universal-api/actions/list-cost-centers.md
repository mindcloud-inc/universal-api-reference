# Conta Azul: List Cost Centers



```
GET https://connect.mindcloud.co/v1/universal/contaAzulAPI/latest/actions/list-cost-centers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Conta Azul `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/contaAzulAPI/latest/actions/list-cost-centers?connectionId=$CONNECTION_ID&pagina=1&tamanho_pagina=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "pagina": "1",
  "tamanho_pagina": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/contaAzulAPI/latest/actions/list-cost-centers?${params}`, {
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
| `pagina` | number | yes | Page number required by Conta Azul. |
| `tamanho_pagina` | number | yes | Page size required by Conta Azul. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "items": [
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
| `items` | array<object> |  |
| `itens_totais` | number |  |
| `totais` | object |  |

## Native endpoint

Through the native Conta Azul API, this operation is `GET /v1/centro-de-custo` (base URL `https://api-v2.contaazul.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-cost-centers.md) for the provider-specific parameters and requirements.

