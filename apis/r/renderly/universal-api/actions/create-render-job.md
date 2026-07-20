# Renderly: Create Render Job

Creates a video render job in Renderly.

```
POST https://connect.mindcloud.co/v1/universal/renderly/latest/actions/create-render-job
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Renderly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/renderly/latest/actions/create-render-job" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/renderly/latest/actions/create-render-job', {
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
| `templateId` | string | no | The template ID to use for template-based rendering. |
| `replacements` | object | no | Template variable replacements keyed by the template's available variables. |
| `width` | number | no | Override video width in pixels. |
| `height` | number | no | Override video height in pixels. |
| `fps` | number | no | Override frames per second. |
| `durationInFrames` | number | no | Override total video duration in frames. |
| `createProject` | boolean | no | Whether to create a project for this render job. |
| `projectName` | string | no | Name for the created project when Create Project is enabled. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `inputProps` | object | no | Complete direct-render configuration object for advanced non-template rendering. |
| `webhookUrl` | string | no | One-off webhook URL to notify when the render completes or fails. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "creditsUsed": 1,
      "estimatedDurationMinutes": 1,
      "jobId": "string",
      "mode": "string",
      "projectId": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `creditsUsed` | number |  |
| `estimatedDurationMinutes` | number |  |
| `jobId` | string |  |
| `mode` | string |  |
| `projectId` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Renderly API, this operation is `POST /renders` (base URL `https://renderly.video/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-render-job.md) for the provider-specific parameters and requirements.

