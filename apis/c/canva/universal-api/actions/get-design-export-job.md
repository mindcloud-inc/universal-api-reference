# Canva: Get Design Export Job

Retrieves a Canva design export job.

```
GET https://connect.mindcloud.co/v1/universal/canva/latest/actions/get-design-export-job
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Canva `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/canva/latest/actions/get-design-export-job?connectionId=$CONNECTION_ID&exportId=e08861ae-3b29-45db-8dc1-1fe0bf7f1cc8" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "exportId": "e08861ae-3b29-45db-8dc1-1fe0bf7f1cc8"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/canva/latest/actions/get-design-export-job?${params}`, {
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
| `exportId` | string | yes | The export job ID. Example: `e08861ae-3b29-45db-8dc1-1fe0bf7f1cc8`. |

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
        "status": "string",
        "urls": [
          "https://example.com"
        ]
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `job.error.code` | string | Provider error code when the export job fails. |
| `job.error.message` | string | Provider error message when the export job fails. |
| `job.id` | string | Canva export job ID. |
| `job.status` | string | Current export job status. |
| `job.urls` | array<string> | Download URLs for a completed export job. |

## Native endpoint

Through the native Canva API, this operation is `GET /v1/exports/:exportId` (base URL `https://api.canva.com/rest`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-design-export-job.md) for the provider-specific parameters and requirements.

