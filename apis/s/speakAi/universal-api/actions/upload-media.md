# Speak Ai: Upload Media

Creates a media file in Speak Ai.

```
POST https://connect.mindcloud.co/v1/universal/speakAi/latest/actions/upload-media
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Speak Ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/speakAi/latest/actions/upload-media" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "url": "https://example.com",
  "mediaType": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/speakAi/latest/actions/upload-media', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "url": "https://example.com",
    "mediaType": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Display name for the media item. |
| `url` | string | yes | Public file URL or AWS signed URL to upload into Speak Ai. |
| `mediaType` | string | yes | Media type to upload, typically audio or video. |
| `description` | string | no | Optional description for the media item. |
| `sourceLanguage` | string | no | Optional BCP 47 language code for the media source language. |
| `tags` | string | no | Comma-separated tags for the media item. |
| `folderId` | string | no | Folder that should contain the uploaded media. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `callbackUrl` | string | no | Optional webhook callback URL for this upload. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "folderId": "string",
      "mediaId": "string",
      "state": "string"
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
| `state` | string |  |

## Native endpoint

Through the native Speak Ai API, this operation is `POST /media/upload` (base URL `https://api.speakai.co/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upload-media.md) for the provider-specific parameters and requirements.

