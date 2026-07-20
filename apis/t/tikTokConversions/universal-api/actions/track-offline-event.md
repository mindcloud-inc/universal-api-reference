# TikTok Conversions: Track Offline Event

Reports an offline event to TikTok Conversions.

```
POST https://connect.mindcloud.co/v1/universal/tikTokConversions/latest/actions/track-offline-event
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TikTok Conversions `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/tikTokConversions/latest/actions/track-offline-event" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "event_set_id": "string",
  "event": "string",
  "timestamp": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/tikTokConversions/latest/actions/track-offline-event', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "event_set_id": "string",
    "event": "string",
    "timestamp": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `event_set_id` | string | yes |  |
| `event` | string | yes |  |
| `event_id` | string | no |  |
| `timestamp` | number | yes |  |
| `context.user.emails[]` | array<string> | no |  |
| `context.user.phone_numbers[]` | array<string> | no |  |
| `properties.order_id` | string | no |  |
| `properties.shop_id` | string | no |  |
| `properties.currency` | string | no |  |
| `properties.value` | number | no |  |
| `properties.event_channel` | string | no |  |
| `properties.contents[].content_id` | string | no |  |
| `properties.contents[].quantity` | number | no |  |
| `properties.contents[].price` | number | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": 1,
      "data": {},
      "message": "string",
      "request_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | number |  |
| `data` | object |  |
| `message` | string |  |
| `request_id` | string |  |

## Native endpoint

Through the native TikTok Conversions API, this operation is `POST /open_api/v1.3/offline/track/` (base URL `https://business-api.tiktok.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/track-offline-event.md) for the provider-specific parameters and requirements.

