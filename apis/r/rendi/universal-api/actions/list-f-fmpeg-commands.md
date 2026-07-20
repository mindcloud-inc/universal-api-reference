# Rendi: List FFmpeg Commands

Retrieves submitted FFmpeg commands from Rendi.

```
GET https://connect.mindcloud.co/v1/universal/rendi/latest/actions/list-f-fmpeg-commands
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rendi `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rendi/latest/actions/list-f-fmpeg-commands?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rendi/latest/actions/list-f-fmpeg-commands?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "command_id": "string",
      "created_at": "2026-05-07T12:00:00.000Z",
      "error_message": "string",
      "error_status": "string",
      "ffmpeg_command_run_seconds": 1,
      "output_file_count": 1,
      "processing_quota_used": 1,
      "processing_seconds": 1,
      "status": "string",
      "storage_quota_used": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `command_id` | string | Unique identifier for the submitted command. |
| `created_at` | date | UTC timestamp when the command was created. |
| `error_message` | string | Provider error message when the command fails. |
| `error_status` | string | Provider error status when the command fails. |
| `ffmpeg_command_run_seconds` | number | FFmpeg execution runtime in seconds. |
| `output_file_count` | number | Number of output files generated. |
| `processing_quota_used` | number | Processing quota consumed. |
| `processing_seconds` | number | Total processing time in seconds. |
| `status` | string | Current status of the FFmpeg command. |
| `storage_quota_used` | number | Storage quota consumed in MB. |

## Native endpoint

Through the native Rendi API, this operation is `GET /v1/commands` (base URL `https://api.rendi.dev`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-f-fmpeg-commands.md) for the provider-specific parameters and requirements.

