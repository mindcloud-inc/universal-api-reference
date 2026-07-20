# Rendi: Poll FFmpeg Command

Retrieves the status of an FFmpeg command in Rendi.

```
GET https://connect.mindcloud.co/v1/universal/rendi/latest/actions/poll-f-fmpeg-command
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rendi `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rendi/latest/actions/poll-f-fmpeg-command?connectionId=$CONNECTION_ID&commandId=123e4567-e89b-12d3-a456-426614174000" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "commandId": "123e4567-e89b-12d3-a456-426614174000"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rendi/latest/actions/poll-f-fmpeg-command?${params}`, {
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
| `commandId` | string | yes | UUID of the FFmpeg command to fetch current status for. Example: `123e4567-e89b-12d3-a456-426614174000`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "command_id": "string",
      "command_type": "string",
      "created_at": "2026-05-07T12:00:00.000Z",
      "error_message": "string",
      "error_status": "string",
      "ffmpeg_command_run_seconds": 1,
      "original_request": {},
      "output_files": {},
      "processing_quota_used": 1,
      "processing_stage": "string",
      "status": "string",
      "total_processing_seconds": 1,
      "vcpu_count": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `command_id` | string | Unique command identifier. |
| `command_type` | string | Command family (FFMPEG_COMMAND or FFMPEG_CHAINED_COMMANDS). |
| `created_at` | date | UTC timestamp when command was created. |
| `error_message` | string | Provider error message when command fails. |
| `error_status` | string | Provider error status when command fails. |
| `ffmpeg_command_run_seconds` | number | FFmpeg runtime on Rendi servers. |
| `original_request` | object | Original submission payload for this command. |
| `output_files` | object | Output file metadata keyed by output alias. |
| `processing_quota_used` | number | Processing quota consumed by this command. |
| `processing_stage` | string | Current processing stage when in progress. |
| `status` | string | Current command status (QUEUED, PROCESSING, SUCCESS, FAILED, etc.). |
| `total_processing_seconds` | number | Total processing time from queue to completion. |
| `vcpu_count` | number | Number of vCPUs used by the command. |

## Native endpoint

Through the native Rendi API, this operation is `GET /v1/commands/:command_id` (base URL `https://api.rendi.dev`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/poll-f-fmpeg-command.md) for the provider-specific parameters and requirements.

