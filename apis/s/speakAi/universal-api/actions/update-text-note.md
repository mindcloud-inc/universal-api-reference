# Speak Ai: Update Text Note

Updates an existing text note in Speak Ai.

```
PUT https://connect.mindcloud.co/v1/universal/speakAi/latest/actions/update-text-note
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Speak Ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/speakAi/latest/actions/update-text-note" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "mediaId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/speakAi/latest/actions/update-text-note', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "mediaId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `mediaId` | string | yes | Speak Ai text note media identifier. |
| `name` | string | no | Updated text note name. |
| `description` | string | no | Updated text note description. |
| `tags[]` | array<string> | no | Updated list of tags for the text note. |
| `text` | string | no | Updated HTML or plain text content. |
| `rawText` | string | no | Updated raw plain-text content. |
| `remark` | string | no | Updated remark for the text note. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string |  |

## Native endpoint

Through the native Speak Ai API, this operation is `PUT /text/update/:mediaId` (base URL `https://api.speakai.co/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-text-note.md) for the provider-specific parameters and requirements.

