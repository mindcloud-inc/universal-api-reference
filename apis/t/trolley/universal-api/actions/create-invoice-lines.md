# Trolley: Create Invoice Lines

Creates new invoice lines in Trolley.

```
POST https://connect.mindcloud.co/v1/universal/trolley/latest/actions/create-invoice-lines
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Trolley `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/trolley/latest/actions/create-invoice-lines" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/trolley/latest/actions/create-invoice-lines', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `invoiceId` | string | no | Invoice ID |

## Response

```json
{
  "success": true,
  "data": [
    {
      "invoice": {},
      "ok": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `invoice` | object |  |
| `ok` | boolean |  |

## Native endpoint

Through the native Trolley API, this operation is `POST /v1/invoices/create-lines` (base URL `https://api.trolley.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-invoice-lines.md) for the provider-specific parameters and requirements.

