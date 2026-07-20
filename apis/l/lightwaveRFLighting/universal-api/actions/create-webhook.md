# LightwaveRF Lighting: Create Webhook

Creates a webhook in LightwaveRF Lighting.

```
POST https://connect.mindcloud.co/v1/universal/lightwaveRFLighting/latest/actions/create-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LightwaveRF Lighting `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/lightwaveRFLighting/latest/actions/create-webhook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "events[]": [
    {}
  ],
  "url": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/lightwaveRFLighting/latest/actions/create-webhook', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "events[]": [{}],
    "url": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `events[]` | array<object> | yes | The list of LightwaveRF event subscriptions to register for the webhook. |
| `url` | string | yes | The public HTTPS URL that should receive webhook deliveries. |
| `ref` | string | no | An optional reference string to correlate the webhook registration. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native LightwaveRF Lighting API returns.

## Native endpoint

Through the native LightwaveRF Lighting API, this operation is `POST /v1/events` (base URL `https://publicapi.lightwaverf.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-webhook.md) for the provider-specific parameters and requirements.

