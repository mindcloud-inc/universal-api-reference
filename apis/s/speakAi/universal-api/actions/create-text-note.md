# Speak Ai: Create Text Note

Creates a text note in Speak Ai.

```
POST https://connect.mindcloud.co/v1/universal/speakAi/latest/actions/create-text-note
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Speak Ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/speakAi/latest/actions/create-text-note" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "text": "string",
  "rawText": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/speakAi/latest/actions/create-text-note', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "text": "string",
    "rawText": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Display name for the text note. |
| `text` | string | yes | HTML or plain text content to display in the editor. |
| `rawText` | string | yes | Raw plain-text content that Speak Ai should analyze. |
| `folderId` | string | no | Optional folder that should contain the text note. |
| `description` | string | no | Optional description for the text note. |
| `tags[]` | array<string> | no | Tags to associate with the text note. |
| `remark` | string | no | Optional remark to store with the text note. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "folderId": "string",
      "mediaId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `folderId` | string |  |
| `mediaId` | string |  |

## Native endpoint

Through the native Speak Ai API, this operation is `POST /text/create` (base URL `https://api.speakai.co/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-text-note.md) for the provider-specific parameters and requirements.

