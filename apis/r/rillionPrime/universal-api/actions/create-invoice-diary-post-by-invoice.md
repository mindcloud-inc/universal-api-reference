# Rillion Prime: Create Invoice Diary Post By Invoice



```
POST https://connect.mindcloud.co/v1/universal/rillionPrime/latest/actions/create-invoice-diary-post-by-invoice
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rillion Prime `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/rillionPrime/latest/actions/create-invoice-diary-post-by-invoice" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "invoiceId": 1,
  "note": "string",
  "attachedFile": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rillionPrime/latest/actions/create-invoice-diary-post-by-invoice', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "invoiceId": 1,
    "note": "string",
    "attachedFile": "string",
    "note": "string",
    "attachedFile": "string",
    "note": "string",
    "attachedFile": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `invoiceId` | number | yes | Path value for InvoiceId. |
| `note` | string | yes | Request body value for Note. |
| `attachedFile` | string | yes | Request body value for AttachedFile. |
| `note` | string | yes | Request body value for Note. |
| `attachedFile` | string | yes | Request body value for AttachedFile. |
| `note` | string | yes | Request body value for Note. |
| `attachedFile` | string | yes | Request body value for AttachedFile. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Rillion Prime API returns.

## Native endpoint

Through the native Rillion Prime API, this operation is `POST /invoice/:invoiceId/diary` (base URL `{{credentials.baseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-invoice-diary-post-by-invoice.md) for the provider-specific parameters and requirements.

