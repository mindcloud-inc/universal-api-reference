# Nudgify: Create Purchase

Creates purchase events in Nudgify.

```
POST https://connect.mindcloud.co/v1/universal/nudgify/latest/actions/create-purchase
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Nudgify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/nudgify/latest/actions/create-purchase" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "orders[]": [
    {}
  ],
  "orders[].orderId": 1,
  "orders[].date": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/nudgify/latest/actions/create-purchase', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "orders[]": [{}],
    "orders[].orderId": 1,
    "orders[].date": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `orders[]` | array<object> | yes | One or more purchase events to send to Nudgify. |
| `orders[].orderId` | number | yes | Integer order identifier for the purchase. |
| `orders[].date` | string | yes | UTC timestamp in `Y-m-d H:i:s` format. |
| `orders[].email` | string | no | Email address tied to the purchase. |
| `orders[].firstName` | string | no | First name to show in the nudge. |
| `orders[].lastName` | string | no | Last name to show in the nudge. |
| `orders[].ip` | string | no | IP address used for location fallback. |
| `orders[].city` | string | no | City to show in the nudge. |
| `orders[].state` | string | no | State or region to show in the nudge. |
| `orders[].country` | string | no | ISO 3166-1 alpha-2 country code. |
| `orders[].lineItems[]` | array<object> | no | Optional line items attached to the purchase. |
| `orders[].lineItems[].itemId` | number | no | Item identifier for a purchased line item. Runtime validation required this to be an integer. |
| `orders[].lineItems[].itemVariationId` | string | no | Variation or SKU identifier for the line item. |
| `orders[].lineItems[].itemName` | string | no | Display name of the purchased item. |
| `orders[].lineItems[].itemLink` | string | no | Product page URL for the purchased item. |
| `orders[].lineItems[].imageUrl` | string | no | Image URL for the purchased item. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Nudgify API returns.

## Native endpoint

Through the native Nudgify API, this operation is `POST /api/purchases` (base URL `https://app.nudgify.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-purchase.md) for the provider-specific parameters and requirements.

