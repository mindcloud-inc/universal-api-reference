# Rendi: Run FFmpeg Command

Submits an FFmpeg command for processing in Rendi.

```
POST https://connect.mindcloud.co/v1/universal/rendi/latest/actions/run-f-fmpeg-command
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rendi `connectionId` ([setup](../authentication.md)).

## Example request

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

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `ffmpegCommand` | string | yes | FFmpeg command string with {{in_*}} and {{out_*}} aliases. Example: `-i {{in_1}} -vf scale=1280:720 {{out_1}}`. |
| `inputFiles` | object | yes | Object mapping in_* aliases to publicly accessible file URLs. Example: `[object Object]`. |
| `outputFiles` | object | yes | Object mapping out_* aliases to output file names. Example: `[object Object]`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `maxCommandRunSeconds` | number | no | Max runtime for a single FFmpeg command (default 300). |
| `vcpuCount` | number | no | Number of virtual CPUs to allocate for this command. |
| `metadata` | object | no | Optional metadata object for tracking/reporting and webhooks. Example: `[object Object]`. |
| `inputCompressedFolder` | string | no | Public URL to a zip archive with input media files. Example: `https://storage.rendi.dev/sample/playlist_sample.zip`. |

## Response

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

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `command_id` | string | Unique identifier assigned to the submitted command. |

## Native endpoint

Through the native Rendi API, this operation is `POST /v1/run-ffmpeg-command` (base URL `https://api.rendi.dev`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/run-f-fmpeg-command.md) for the provider-specific parameters and requirements.

