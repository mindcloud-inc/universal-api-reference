# Seam: Update Webhook

Updates an existing webhook in Seam.

```
PUT https://connect.mindcloud.co/v1/universal/seam/latest/actions/update-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Seam `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/seam/latest/actions/update-webhook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "eventTypes": "string",
  "webhookId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/seam/latest/actions/update-webhook', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "eventTypes": "string",
    "webhookId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `eventTypes` | list<string> | yes | Required array of webhook event types. Seam expects `event_types` as an array of strings; the current execution surface is serializing this as a string and the provider rejects the request. |
| `webhookId` | string | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Seam API returns.

## Native endpoint

Through the native Seam API, this operation is `POST /webhooks/update` (base URL `https://connect.getseam.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-webhook.md) for the provider-specific parameters and requirements.

