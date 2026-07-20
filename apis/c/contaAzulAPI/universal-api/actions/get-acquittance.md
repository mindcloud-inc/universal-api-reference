# Conta Azul: Get Acquittance



```
GET https://connect.mindcloud.co/v1/universal/contaAzulAPI/latest/actions/get-acquittance
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Conta Azul `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/contaAzulAPI/latest/actions/get-acquittance?connectionId=$CONNECTION_ID&baixa_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "baixa_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/contaAzulAPI/latest/actions/get-acquittance?${params}`, {
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
| `baixa_id` | string | yes | Conta Azul acquittance identifier from the path. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "conta_financeira": {},
      "data_pagamento": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "observacao": "string",
      "valor_composicao": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `conta_financeira` | object |  |
| `data_pagamento` | date |  |
| `id` | string |  |
| `observacao` | string |  |
| `valor_composicao` | number |  |

## Native endpoint

Through the native Conta Azul API, this operation is `GET /v1/financeiro/eventos-financeiros/parcelas/baixa/{baixa_id}` (base URL `https://api-v2.contaazul.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-acquittance.md) for the provider-specific parameters and requirements.

