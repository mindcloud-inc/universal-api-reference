# Canva: Create URL Import Job

Creates a Canva URL import job.

```
POST https://connect.mindcloud.co/v1/universal/canva/latest/actions/create-url-import-job
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Canva `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/canva/latest/actions/create-url-import-job" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "title": "My Awesome Design",
  "url": "https://example.com/presentation.key"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/canva/latest/actions/create-url-import-job', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "title": "My Awesome Design",
    "url": "https://example.com/presentation.key"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `title` | string | yes | A title for the design. Example: `My Awesome Design`. |
| `url` | string | yes | The public URL of the file to import. Example: `https://example.com/presentation.key`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `mimeType` | string | no | Optional MIME type of the imported file. Example: `application/vnd.apple.keynote`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "job": {
        "error": {
          "code": "string",
          "message": "string"
        },
        "id": "string",
        "result": {
          "designs": {
            "id": "string",
            "title": "string"
          }
        },
        "status": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `job.error.code` | string | Provider error code when the URL import job fails. |
| `job.error.message` | string | Provider error message when the URL import job fails. |
| `job.id` | string | Canva URL import job ID. |
| `job.result.designs` | array<object> | Imported Canva designs when the job succeeds. |
| `job.result.designs.id` | string | Imported Canva design ID. |
| `job.result.designs.title` | string | Imported Canva design title. |
| `job.status` | string | Current URL import job status. |

## Native endpoint

Through the native Canva API, this operation is `POST /v1/url-imports` (base URL `https://api.canva.com/rest`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-url-import-job.md) for the provider-specific parameters and requirements.

