# Sumtracker: Perform Purchase Order Action

Performs an action on a purchase order in Sumtracker.

```
PUT https://connect.mindcloud.co/v1/universal/sumtracker/latest/actions/perform-order-action
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sumtracker `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/sumtracker/latest/actions/perform-order-action" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "action": "string",
  "document_type": "string",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sumtracker/latest/actions/perform-order-action', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "action": "string",
    "document_type": "string",
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `action` | string | yes | Action to perform, such as `mark-incoming`, `close`, `cancel`, or `generate-pdf`. |
| `document_type` | string | yes | Use `orders` for purchase orders or `stock-transfers` for stock transfers. |
| `id` | string | yes | Purchase order or stock transfer ID. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Sumtracker API returns.

## Native endpoint

Through the native Sumtracker API, this operation is `PUT /api/version/2025-03/purchases/:document_type/perform_action/:id/:action/` (base URL `https://inventory-api.sumtracker.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/perform-order-action.md) for the provider-specific parameters and requirements.

