# Moderation API: Analyze Audio

Submits audio to Moderation API for analysis.

```
POST https://connect.mindcloud.co/v1/universal/moderationAPI/latest/actions/analyze-audio
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Moderation API `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/moderationAPI/latest/actions/analyze-audio" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "url": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/moderationAPI/latest/actions/analyze-audio', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "url": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `url` | string | yes | The URL of the audio you want to analyze. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `contentId` | string | no | The unique ID of the content in your database. |
| `channelKey` | string | no | The key of the channel. |
| `doNotStore` | boolean | no | Do not store the content. The content won't enter the review queue |
| `authorId` | string | no | The author of the content. |
| `contextId` | string | no | For example the ID of a chat room or a post |
| `metadata` | object | no | Any metadata you want to store with the content |

## Response

```json
{
  "success": true,
  "data": [
    {
      "author": {},
      "contentId": "string",
      "error": "string",
      "flagged": true,
      "request": {},
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `author` | object |  |
| `contentId` | string | The ID of the content. Only returned if the content was stored. |
| `error` | string | Error message if the request failed |
| `flagged` | boolean | Whether the content was flagged by any models |
| `request` | object | Information about the request |
| `status` | string | Success if the request was successful |

## Native endpoint

Through the native Moderation API API, this operation is `POST /moderate/audio` (base URL `https://api.moderationapi.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/analyze-audio.md) for the provider-specific parameters and requirements.

