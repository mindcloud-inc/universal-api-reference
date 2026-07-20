# Billingo: Copy Document

Creates a copy of a document in Billingo.

```
POST https://connect.mindcloud.co/v1/universal/billingo/latest/actions/copy-document
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Billingo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/billingo/latest/actions/copy-document" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "0"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/billingo/latest/actions/copy-document', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "0"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes | Billingo document ID to copy. Default: `0`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "currency": "string",
      "gross_total": 1,
      "id": 1,
      "invoice_number": "string",
      "payment_status": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `currency` | string | Document currency. |
| `gross_total` | number | Gross total. |
| `id` | number | Copied document ID. |
| `invoice_number` | string | Document invoice number. |
| `payment_status` | string | Document payment status. |
| `type` | string | Document type. |

## Native endpoint

Through the native Billingo API, this operation is `POST /documents/:id/copy` (base URL `https://api.billingo.hu/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/copy-document.md) for the provider-specific parameters and requirements.

