# DynaPictures: Subscribe Webhook

Creates a webhook subscription in DynaPictures.

```
POST https://connect.mindcloud.co/v1/universal/dynaPictures/latest/actions/subscribe-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DynaPictures `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/dynaPictures/latest/actions/subscribe-webhook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "targetUrl": "https://example.com",
  "templateId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dynaPictures/latest/actions/subscribe-webhook', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "targetUrl": "https://example.com",
    "templateId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `targetUrl` | string | yes | Webhook URL that will receive notifications. |
| `templateId` | string | yes | UID of the template to watch. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native DynaPictures API returns.

## Native endpoint

Through the native DynaPictures API, this operation is `POST /hooks` (base URL `https://api.dynapictures.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/subscribe-webhook.md) for the provider-specific parameters and requirements.

