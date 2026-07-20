# YouTube: Update Channel

Updates an existing channel in YouTube.

```
PUT https://connect.mindcloud.co/v1/universal/youtube/latest/actions/update-channel
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a YouTube `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/youtube/latest/actions/update-channel" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "part": "brandingSettings",
  "id": "UC_x5XG1OV2P6uZZ5FSM9Ttw"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/youtube/latest/actions/update-channel', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "part": "brandingSettings",
    "id": "UC_x5XG1OV2P6uZZ5FSM9Ttw"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `part` | string | yes | Accepts multiple values in one string, delimited by `,`. Example: `brandingSettings`. |
| `id` | string | yes | Example: `UC_x5XG1OV2P6uZZ5FSM9Ttw`. |
| `brandingSettings` | object | no | Example: `[object Object]`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `invideoPromotion` | object | no | Example: `[object Object]`. |
| `onBehalfOfContentOwner` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "brandingSettings": {
        "channel": {
          "description": "string",
          "title": "string"
        }
      },
      "etag": "string",
      "id": "string",
      "kind": "string",
      "snippet": {
        "customUrl": "https://example.com",
        "title": "string"
      },
      "statistics": {
        "subscriberCount": "string",
        "videoCount": "string"
      },
      "status": {
        "privacyStatus": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `brandingSettings.channel.description` | string |  |
| `brandingSettings.channel.title` | string |  |
| `etag` | string |  |
| `id` | string |  |
| `kind` | string |  |
| `snippet.customUrl` | string |  |
| `snippet.title` | string |  |
| `statistics.subscriberCount` | string |  |
| `statistics.videoCount` | string |  |
| `status.privacyStatus` | string |  |

## Native endpoint

Through the native YouTube API, this operation is `PUT /youtube/v3/channels` (base URL `https://www.googleapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-channel.md) for the provider-specific parameters and requirements.

