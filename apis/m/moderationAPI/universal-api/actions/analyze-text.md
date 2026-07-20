# Moderation API: Analyze Text

Submits text to Moderation API for analysis.

```
POST https://connect.mindcloud.co/v1/universal/moderationAPI/latest/actions/analyze-text
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Moderation API `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/moderationAPI/latest/actions/analyze-text" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "value": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/moderationAPI/latest/actions/analyze-text', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "value": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `value` | string | yes | The text you'd like to analyze. We recommend to submit plain text or HTML |

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
      "author": "string",
      "content": "string",
      "content_moderated": true,
      "contentId": "string",
      "data_found": true,
      "flagged": true,
      "original": "string",
      "request": {},
      "status": "string",
      "unicode_spoofing": true,
      "wordlists": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `author` | string |  |
| `content` | string |  |
| `content_moderated` | boolean |  |
| `contentId` | string |  |
| `data_found` | boolean |  |
| `flagged` | boolean |  |
| `original` | string |  |
| `request` | object |  |
| `status` | string |  |
| `unicode_spoofing` | boolean |  |
| `wordlists` | array |  |

## Native endpoint

Through the native Moderation API API, this operation is `POST /moderate/text` (base URL `https://api.moderationapi.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/analyze-text.md) for the provider-specific parameters and requirements.

