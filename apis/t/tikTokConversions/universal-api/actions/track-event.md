# TikTok Conversions: Track Event

Reports a web event to TikTok Conversions.

```
POST https://connect.mindcloud.co/v1/universal/tikTokConversions/latest/actions/track-event
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TikTok Conversions `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/tikTokConversions/latest/actions/track-event" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "data[].event": "string",
  "data[].event_time": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/tikTokConversions/latest/actions/track-event', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "data[].event": "string",
    "data[].event_time": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `data[].event` | string | yes | Standard or custom TikTok event name. |
| `data[].event_time` | number | yes | Unix timestamp in seconds for when the event occurred. |
| `data[].event_id` | string | no | Optional deduplication identifier shared with Pixel events. |
| `data[].limited_data_use` | boolean | no | Optional limited data use flag. |
| `data[].user.email` | string | no | User email. TikTok recommends SHA-256 hashing when applicable. |
| `data[].user.phone` | string | no | User phone number. TikTok recommends SHA-256 hashing when applicable. |
| `data[].user.external_id` | string | no | Advertiser-defined customer identifier. |
| `data[].user.ttclid` | string | no | TikTok click identifier from the landing URL. |
| `data[].user.ttp` | string | no | TikTok first-party cookie value. |
| `data[].user.ip` | string | no | Client IP address. |
| `data[].user.user_agent` | string | no | Client user agent string. |
| `data[].properties.currency` | string | no | ISO currency code for the event value. |
| `data[].properties.value` | number | no | Monetary value for the event. |
| `data[].properties.content_type` | string | no | TikTok content type, such as product or product_group. |
| `data[].properties.query` | string | no | Search query associated with the event. |
| `data[].properties.description` | string | no | Description associated with the tracked event. |
| `data[].properties.contents[].price` | number | no | Item price. |
| `data[].properties.contents[].quantity` | number | no | Item quantity. |
| `data[].properties.contents[].content_id` | string | no | Catalog or product identifier. |
| `data[].properties.contents[].content_category` | string | no | Category for the content item. |
| `data[].properties.contents[].content_name` | string | no | Name of the content item. |
| `data[].properties.contents[].brand` | string | no | Brand associated with the content item. |
| `data[].page.url` | string | no | URL of the page where the event occurred. |
| `data[].page.referrer` | string | no | Referrer URL for the page view. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `testEventCode` | string | no | Optional TikTok test event code for non-production validation. |

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
| `code` | number | TikTok provider status code returned by the Events API. |
| `data` | object | Provider response payload object. |
| `message` | string | Provider response message. |
| `request_id` | string | TikTok request identifier for support and debugging. |

## Native endpoint

Through the native TikTok Conversions API, this operation is `POST /open_api/v1.3/event/track/` (base URL `https://business-api.tiktok.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/track-event.md) for the provider-specific parameters and requirements.

