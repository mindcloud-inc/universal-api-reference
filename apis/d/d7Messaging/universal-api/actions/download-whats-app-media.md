# D7 Messaging: Download WhatsApp Media

Downloads WhatsApp media from D7 Messaging.

```
GET https://connect.mindcloud.co/v1/universal/d7Messaging/latest/actions/download-whats-app-media
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a D7 Messaging `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/d7Messaging/latest/actions/download-whats-app-media?connectionId=$CONNECTION_ID&mediaId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "mediaId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/d7Messaging/latest/actions/download-whats-app-media?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `mediaId` | string | yes | Media ID returned by a WhatsApp media message. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "detail": {
        "code": "string",
        "message": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `detail.code` | string |  |
| `detail.message` | string |  |

## Native endpoint

Through the native D7 Messaging API, this operation is `GET /whatsapp/v2/download/:media_id` (base URL `https://api.d7networks.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/download-whats-app-media.md) for the provider-specific parameters and requirements.

