# Trint: Upload and Transcribe

Uploads and transcribes a file in Trint.

```
POST https://connect.mindcloud.co/v1/universal/trint/latest/actions/upload-and-transcribe
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Trint `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/trint/latest/actions/upload-and-transcribe" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/trint/latest/actions/upload-and-transcribe', {
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



## Response

```json
{
  "success": true,
  "data": [
    {
      "created": "2026-05-07T12:00:00.000Z",
      "duration": 1,
      "excerpt": "string",
      "fileType": "string",
      "folderId": "string",
      "id": "string",
      "language": "string",
      "metadata": "string",
      "notes": "string",
      "timecode": "string",
      "timecodeOffsetEnabled": true,
      "title": "string",
      "updated": "2026-05-07T12:00:00.000Z",
      "workspaceId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created` | date | Creation timestamp. |
| `duration` | number | Transcript duration in milliseconds. |
| `excerpt` | string | Transcript excerpt preview. |
| `fileType` | string | Trint file type. |
| `folderId` | string | Folder identifier when present. |
| `id` | string | Trint file identifier. |
| `language` | string | Transcript language code. |
| `metadata` | string | User-supplied transcript metadata. |
| `notes` | string | Transcript notes. |
| `timecode` | string | Transcript start timecode. |
| `timecodeOffsetEnabled` | boolean | Whether timecode offset is enabled. |
| `title` | string | Transcript title. |
| `updated` | date | Last update timestamp. |
| `workspaceId` | string | Shared drive identifier when present. |

## Native endpoint

Through the native Trint API, this operation is `POST https://upload.trint.com/` (base URL `https://api.trint.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upload-and-transcribe.md) for the provider-specific parameters and requirements.

