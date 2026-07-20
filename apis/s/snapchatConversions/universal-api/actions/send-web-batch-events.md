# Snapchat Conversions: Send Web Batch Events

Creates a batch of web conversion events in Snapchat Conversions.

```
POST https://connect.mindcloud.co/v1/universal/snapchatConversions/latest/actions/send-web-batch-events
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Snapchat Conversions `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/snapchatConversions/latest/actions/send-web-batch-events" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "pixelId": "string",
  "data": {},
  "data[].eventName": "Ava Chen",
  "data[].eventTime": 1,
  "data[].eventSourceUrl": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/snapchatConversions/latest/actions/send-web-batch-events', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "pixelId": "string",
    "data": {},
    "data[].eventName": "Ava Chen",
    "data[].eventTime": 1,
    "data[].eventSourceUrl": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `pixelId` | string | yes | Snapchat Pixel ID that owns the web events. |
| `data` | list<object> | yes | Array of web conversion events to send in one request. |
| `data[].eventName` | string | yes | Snap standard or custom event name for the web event. |
| `data[].eventTime` | number | yes | Epoch timestamp in seconds or milliseconds for when the event happened. |
| `data[].eventSourceUrl` | string | yes | Web page URL where the event took place. |
| `data[].userData` | object | no | User matching fields for the event. |
| `data[].userData.clientIpAddress` | string | no | Device IP address for matching. Do not hash. |
| `data[].userData.clientUserAgent` | string | no | Device user agent string. Recommended for web events. |
| `data[].userData.em` | list<string> | no | Normalized SHA-256 email hashes for user matching. |
| `data[].eventId` | string | no | Unique event identifier used for deduplication. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Snapchat Conversions API returns.

## Native endpoint

Through the native Snapchat Conversions API, this operation is `POST https://tr.snapchat.com/v3/:pixel_id/events` (base URL `https://adsapi.snapchat.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-web-batch-events.md) for the provider-specific parameters and requirements.

