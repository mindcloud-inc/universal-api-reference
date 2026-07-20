# Murf Dub: Create Dubbing Job With Project ID

Creates a dubbing job in Murf Dub from a project.

```
POST https://connect.mindcloud.co/v1/universal/murfDub/latest/actions/create-dubbing-job-with-project-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Murf Dub `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/murfDub/latest/actions/create-dubbing-job-with-project-id" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "projectId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/murfDub/latest/actions/create-dubbing-job-with-project-id', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "projectId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `projectId` | string | yes | Existing Murf Dub project ID. |
| `file` | file | no | The media file to upload for dubbing. |
| `fileUrl` | string | no | Public URL of the media file to dub. |
| `webhookUrl` | string | no | Webhook URL for job status notifications. |
| `fileName` | string | no | Reference name for the upload. |
| `priority` | string | no | Processing priority. |
| `webhookSecret` | string | no | Secret used to validate webhook calls. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "dubbing_type": "string",
      "file_name": "Ava Chen",
      "file_url": "https://example.com",
      "job_id": "string",
      "priority": "string",
      "source_locale": "string",
      "target_locales": [
        "string"
      ],
      "warning": "string",
      "webhook_url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `dubbing_type` | string | Murf dubbing mode used for the job. |
| `file_name` | string | Source file name recorded for the job. |
| `file_url` | string | Public URL of the dubbed source file. |
| `job_id` | string | Murf job identifier. |
| `priority` | string | Processing priority assigned to the job. |
| `source_locale` | string | Source locale resolved for the project-backed job. |
| `target_locales` | array<string> | Target locales configured on the project. |
| `warning` | string | Provider warning returned during job creation. |
| `webhook_url` | string | Webhook URL configured for job notifications. |

## Native endpoint

Through the native Murf Dub API, this operation is `POST /v1/murfdub/jobs/create-with-project-id` (base URL `https://api.murf.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-dubbing-job-with-project-id.md) for the provider-specific parameters and requirements.

