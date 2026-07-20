# Rendi Universal API Examples

These examples use the MindCloud API key and Rendi connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List FFmpeg Commands

Retrieves submitted FFmpeg commands from Rendi.

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

Example response:

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

See the full [List FFmpeg Commands action reference](actions/list-f-fmpeg-commands.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/rendi/latest/actions/list-f-fmpeg-commands).

## Run FFmpeg Command

Submits an FFmpeg command for processing in Rendi.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/rendi/latest/actions/run-f-fmpeg-command" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "ffmpegCommand": "-i {{in_1}} -vf scale=1280:720 {{out_1}}",
  "inputFiles": "[object Object]",
  "outputFiles": "[object Object]"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rendi/latest/actions/run-f-fmpeg-command', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "ffmpegCommand": "-i {{in_1}} -vf scale=1280:720 {{out_1}}",
    "inputFiles": "[object Object]",
    "outputFiles": "[object Object]"
  })
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [
    {
      "command_id": "string"
    }
  ],
  "meta": {}
}
```

See the full [Run FFmpeg Command action reference](actions/run-f-fmpeg-command.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/rendi/latest/actions/run-f-fmpeg-command).
