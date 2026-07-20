# Canva: Get URL Import Job

Retrieves a Canva URL import job.

```
GET https://connect.mindcloud.co/v1/universal/canva/latest/actions/get-url-import-job
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Canva `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/canva/latest/actions/get-url-import-job?connectionId=$CONNECTION_ID&jobId=f81b26fd-a33d-4c2d-9e8c-4a7aca798b17" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "jobId": "f81b26fd-a33d-4c2d-9e8c-4a7aca798b17"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/canva/latest/actions/get-url-import-job?${params}`, {
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
| `jobId` | string | yes | The URL import job ID. Example: `f81b26fd-a33d-4c2d-9e8c-4a7aca798b17`. |

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

Through the native Canva API, this operation is `GET /v1/url-imports/:jobId` (base URL `https://api.canva.com/rest`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-url-import-job.md) for the provider-specific parameters and requirements.

