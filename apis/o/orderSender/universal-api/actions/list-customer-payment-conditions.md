# Order Sender: List Customer Payment Conditions

Retrieves customer payment conditions from Order Sender.

```
GET https://connect.mindcloud.co/v1/universal/orderSender/latest/actions/list-customer-payment-conditions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Order Sender `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/orderSender/latest/actions/list-customer-payment-conditions?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/orderSender/latest/actions/list-customer-payment-conditions?${params}`, {
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
| `delimiter` | string | no | Delimiter used only when requesting CSV output. |
| `format` | string | no | Response format. Use json for structured records. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "codice_clienti": "string",
      "codice_condizione_pagamento": "string",
      "codice_fornitori": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `codice_clienti` | string |  |
| `codice_condizione_pagamento` | string |  |
| `codice_fornitori` | string |  |

## Native endpoint

Through the native Order Sender API, this operation is `GET /op/export/res/clienti_pagamenti` (base URL `https://business.ordersender.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-customer-payment-conditions.md) for the provider-specific parameters and requirements.

