# Shopper Approved: Create Review Entry

Creates a new review entry in Shopper Approved.

```
POST https://connect.mindcloud.co/v1/universal/shopperApproved/latest/actions/create-review-entry
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Shopper Approved `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/shopperApproved/latest/actions/create-review-entry" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "email": "customer@example.com",
  "followup": "2026-03-31",
  "orderId": "ORDER-1001"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/shopperApproved/latest/actions/create-review-entry', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "email": "customer@example.com",
    "followup": "2026-03-31",
    "orderId": "ORDER-1001"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `email` | string | yes | The customer's email address. Example: `customer@example.com`. |
| `followup` | date | yes | The follow-up date in YYYY-MM-DD format. Example: `2026-03-31`. |
| `orderId` | string | yes | The unique order ID. Example: `ORDER-1001`. |
| `name` | string | no | The customer's name. Example: `Jane Doe`. |
| `products` | string | no | Comma-separated product IDs to attach to the review. Example: `sku-1,sku-2`. |
| `test` | boolean | no | Whether the review entry is a test. Default: `false`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `customQuestions` | string | no | A JSON-encoded object of custom question values. Example: `JSON string like question=answer`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Shopper Approved API returns.

## Native endpoint

Through the native Shopper Approved API, this operation is `POST /reviews/:siteid` (base URL `https://api.shopperapproved.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-review-entry.md) for the provider-specific parameters and requirements.

