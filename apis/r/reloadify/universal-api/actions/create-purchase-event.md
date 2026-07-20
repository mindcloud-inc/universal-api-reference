# Reloadify: Create Purchase Event

Creates a server-side purchase event in Reloadify.

```
POST https://connect.mindcloud.co/v1/universal/reloadify/latest/actions/create-purchase-event
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Reloadify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/reloadify/latest/actions/create-purchase-event" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "languageId": "string",
  "purchase_event.order_id": "string",
  "purchase_event.profile_id": "string",
  "purchase_event.visitor_token": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/reloadify/latest/actions/create-purchase-event', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "languageId": "string",
    "purchase_event.order_id": "string",
    "purchase_event.profile_id": "string",
    "purchase_event.visitor_token": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `languageId` | string | yes | Reloadify language ID. |
| `purchase_event.order_id` | string | yes | Existing order ID. |
| `purchase_event.profile_id` | string | yes | Existing profile ID. |
| `purchase_event.visitor_token` | string | yes | Reloadify tracking visitor token. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Reloadify API returns.

## Native endpoint

Through the native Reloadify API, this operation is `PUT /v2/languages/:language_id/purchase_events` (base URL `https://api.reloadify.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-purchase-event.md) for the provider-specific parameters and requirements.

