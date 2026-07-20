# Canva: Get URL Asset Upload Job

Retrieves a Canva URL asset upload job.

```
GET https://connect.mindcloud.co/v1/universal/canva/latest/actions/get-url-asset-upload-job
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Canva `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/canva/latest/actions/get-url-asset-upload-job?connectionId=$CONNECTION_ID&jobId=84c741e4-c8d7-4ef3-bd9a-778dc1ed3d93" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "jobId": "84c741e4-c8d7-4ef3-bd9a-778dc1ed3d93"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/canva/latest/actions/get-url-asset-upload-job?${params}`, {
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
| `jobId` | string | yes | The asset upload job ID. Example: `84c741e4-c8d7-4ef3-bd9a-778dc1ed3d93`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "job": {
        "asset": {
          "id": "string",
          "name": "Ava Chen",
          "tags": [
            "string"
          ],
          "type": "string"
        },
        "error": {
          "code": "string"
        },
        "id": "string",
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
| `job.asset.id` | string | Uploaded Canva asset ID when the job succeeds. |
| `job.asset.name` | string | Uploaded asset name when the job succeeds. |
| `job.asset.tags` | array<string> | Uploaded asset tags when present. |
| `job.asset.type` | string | Uploaded asset type when the job succeeds. |
| `job.error.code` | string | Provider error code when the job fails. |
| `job.id` | string | Canva URL asset upload job ID. |
| `job.status` | string | Current job status. |

## Native endpoint

Through the native Canva API, this operation is `GET /v1/url-asset-uploads/:jobId` (base URL `https://api.canva.com/rest`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-url-asset-upload-job.md) for the provider-specific parameters and requirements.

