# TikTok Conversions: Track Pixel Event

Tracks a Pixel event in TikTok Conversions.

```
POST https://connect.mindcloud.co/v1/universal/tikTokConversions/latest/actions/track-pixel-event
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TikTok Conversions `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/tikTokConversions/latest/actions/track-pixel-event" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "event": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/tikTokConversions/latest/actions/track-pixel-event', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "event": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `event` | string | yes |  |
| `event_id` | string | no |  |
| `timestamp` | number | no |  |
| `context.ad.callback` | string | no |  |
| `context.page.url` | string | no |  |
| `context.page.referrer` | string | no |  |
| `context.user.external_id` | string | no |  |
| `context.user.email` | string | no |  |
| `context.user.phone_number` | string | no |  |
| `context.user.ttp` | string | no |  |
| `context.ip` | string | no |  |
| `context.user_agent` | string | no |  |
| `properties.content_type` | string | no |  |
| `properties.currency` | string | no |  |
| `properties.value` | number | no |  |
| `properties.query` | string | no |  |
| `properties.description` | string | no |  |
| `properties.status` | string | no |  |
| `properties.contents[].price` | number | no |  |
| `properties.contents[].quantity` | number | no |  |
| `properties.contents[].content_id` | string | no |  |
| `properties.contents[].content_category` | string | no |  |
| `properties.contents[].content_name` | string | no |  |
| `properties.contents[].brand` | string | no |  |

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

Through the native TikTok Conversions API, this operation is `POST /open_api/v1.3/pixel/track/` (base URL `https://business-api.tiktok.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/track-pixel-event.md) for the provider-specific parameters and requirements.

