# Speak Ai: Update Media

Updates an existing media item in Speak Ai.

```
PUT https://connect.mindcloud.co/v1/universal/speakAi/latest/actions/update-media
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Speak Ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/speakAi/latest/actions/update-media" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "mediaId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/speakAi/latest/actions/update-media', {
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
| `mediaId` | string | yes | Speak Ai media identifier. |
| `name` | string | no | Optional new media name. |
| `description` | string | no | Optional new media description. |
| `tags[]` | array<string> | no | Optional list of tags for the media item. |

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

Through the native Speak Ai API, this operation is `PUT /media/:mediaId` (base URL `https://api.speakai.co/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-media.md) for the provider-specific parameters and requirements.

