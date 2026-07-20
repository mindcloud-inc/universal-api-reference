# Conta Azul: Get Financial Installment



```
GET https://connect.mindcloud.co/v1/universal/contaAzulAPI/latest/actions/get-financial-installment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Conta Azul `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/contaAzulAPI/latest/actions/get-financial-installment?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/contaAzulAPI/latest/actions/get-financial-installment?${params}`, {
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
| `id` | string | yes | Conta Azul installment identifier from the path. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data_vencimento": "2026-05-07T12:00:00.000Z",
      "evento": {},
      "id": "string",
      "referencia": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data_vencimento` | date |  |
| `evento` | object |  |
| `id` | string |  |
| `referencia` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Conta Azul API, this operation is `GET /v1/financeiro/eventos-financeiros/parcelas/{id}` (base URL `https://api-v2.contaazul.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-financial-installment.md) for the provider-specific parameters and requirements.

