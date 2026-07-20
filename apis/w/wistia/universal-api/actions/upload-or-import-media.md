# Wistia: Upload Or Import Media

Uploads a media file to Wistia or imports one by URL.

```
POST https://connect.mindcloud.co/v1/universal/wistia/latest/actions/upload-or-import-media
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Wistia `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/wistia/latest/actions/upload-or-import-media" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/wistia/latest/actions/upload-or-import-media', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `url` | string | no |  |
| `projectId` | string | no |  |
| `name` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created": "2026-05-07T12:00:00.000Z",
      "duration": 1,
      "hashedId": "string",
      "id": 1,
      "name": "Ava Chen",
      "progress": 1,
      "thumbnail": {
        "height": 1,
        "url": "https://example.com",
        "width": 1
      },
      "type": "string",
      "updated": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created` | date | The date when the media was originally uploaded. |
| `duration` | number | Specifies the length (in seconds) for audio and video files. |
| `hashedId` | string | A unique alphanumeric identifier for this media. |
| `id` | number | A unique numeric identifier for the media within the system. |
| `name` | string | The display name of the media. |
| `progress` | number | A floating point value between 0 and 1 that indicates the progress of the processing for this file. |
| `thumbnail` | object |  |
| `thumbnail.height` | number |  |
| `thumbnail.url` | string |  |
| `thumbnail.width` | number |  |
| `type` | string | A string representing what type of media this is. |
| `updated` | date | The date when the media was last changed. |

## Native endpoint

Through the native Wistia API, this operation is `POST https://upload.wistia.com/` (base URL `https://api.wistia.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upload-or-import-media.md) for the provider-specific parameters and requirements.

