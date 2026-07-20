# Trint: Retrieve File

Retrieves a file from your Trint account.

```
GET https://connect.mindcloud.co/v1/universal/trint/latest/actions/retrieve-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Trint `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/trint/latest/actions/retrieve-file?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/trint/latest/actions/retrieve-file?${params}`, {
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
| `id` | string | yes | The Trint file identifier to retrieve. |

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

Through the native Trint API, this operation is `GET /transcripts/file/:id` (base URL `https://api.trint.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-file.md) for the provider-specific parameters and requirements.

