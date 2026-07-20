# ProveSource: Send Webhook Event



```
POST https://connect.mindcloud.co/v1/universal/proveSource/latest/actions/send-webhook-event
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ProveSource `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/proveSource/latest/actions/send-webhook-event" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "webhookId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/proveSource/latest/actions/send-webhook-event', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "webhookId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `webhookId` | string | yes | The ProveSource notification webhook identifier to send this event to. |
| `email` | string | no | Email for the conversion or lead. Required for Stream notifications. |
| `firstName` | string | no | Lead first name shown in the notification when available. |
| `lastName` | string | no | Lead last name shown in the notification when available. |
| `timestamp` | number | no | Event timestamp in milliseconds or seconds. |
| `ip` | string | no | Visitor IP address used for location lookup. |
| `guid` | string | no | Optional product or category identifier used by ProveSource webhook notifications. |
| `city` | string | no | Optional city value for location enrichment. |
| `state` | string | no | Optional state name for US locations. |
| `stateCode` | string | no | Optional state code for US locations. |
| `country` | string | no | Optional country value for location enrichment. |
| `countryCode` | string | no | Optional two-letter country code for location enrichment. |
| `productName` | string | no | Optional product name appended to the notification text. |
| `productLink` | string | no | Optional product page URL used for click-through behavior. |
| `productImage` | string | no | Optional product image URL shown in the notification. |
| `total` | number | no | Optional purchase total amount. |
| `currency` | string | no | Optional purchase currency code. |
| `products[]` | array<object> | no | Optional array of product line items for multi-product purchases. Each item should include at least a name and link. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native ProveSource API returns.

## Native endpoint

Through the native ProveSource API, this operation is `POST /webhooks/track/:webhookId` (base URL `https://api.provesrc.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-webhook-event.md) for the provider-specific parameters and requirements.

