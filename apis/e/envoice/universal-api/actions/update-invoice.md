# Envoice: Update Invoice

Updates an existing invoice in Envoice.

```
PUT https://connect.mindcloud.co/v1/universal/envoice/latest/actions/update-invoice
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Envoice `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/envoice/latest/actions/update-invoice" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1,
  "clientId": 1,
  "number": "string",
  "issuedOn": "2026-05-07T12:00:00.000Z",
  "duedate": "2026-05-07T12:00:00.000Z",
  "status": "string",
  "currencyId": 1,
  "paymentGateways": "string",
  "items": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/envoice/latest/actions/update-invoice', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1,
    "clientId": 1,
    "number": "string",
    "issuedOn": "2026-05-07T12:00:00.000Z",
    "duedate": "2026-05-07T12:00:00.000Z",
    "status": "string",
    "currencyId": 1,
    "paymentGateways": "string",
    "items": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes | Invoice identifier to update. |
| `clientId` | number | yes | Envoice client identifier for the invoice. |
| `number` | string | yes | Invoice number to assign in Envoice. |
| `issuedOn` | date | yes | Invoice issue date. |
| `duedate` | date | yes | Invoice due date. Envoice expects the field name Duedate. |
| `status` | string | yes | Invoice status value accepted by Envoice, such as Draft. |
| `currencyId` | number | yes | Currency identifier for the invoice. |
| `paymentGateways` | string<object> | yes | Payment gateway JSON array accepted by Envoice, for example [{"Name":"paypal"}]. |
| `items` | string<object> | yes | Invoice line items JSON array accepted by Envoice. Include existing item Id values when updating existing lines. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Success` | boolean | Whether the invoice update succeeded. |

## Native endpoint

Through the native Envoice API, this operation is `POST invoice/update` (base URL `https://www.envoice.in/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-invoice.md) for the provider-specific parameters and requirements.

