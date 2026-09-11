# Peplink: Create Order PO File

Create a customer PO File for an order.

```
POST https://connect.mindcloud.co/v1/universal/peplink/latest/actions/create-order-po-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Peplink `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/peplink/latest/actions/create-order-po-file" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "orderNumber": "string",
  "fileName": "Ava Chen",
  "fileContentInBase64": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/peplink/latest/actions/create-order-po-file', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "orderNumber": "string",
    "fileName": "Ava Chen",
    "fileContentInBase64": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `orderNumber` | string | yes |  |
| `fileName` | string | yes |  |
| `fileContentInBase64` | string | yes | File content after converted into base 64. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Peplink API returns.

## Native endpoint

Through the native Peplink API, this operation is `POST orders/:orderNumber/customer-po-files` (base URL `https://portal.peplink.com/api/e/v1/cp/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-order-po-file.md) for the provider-specific parameters and requirements.

