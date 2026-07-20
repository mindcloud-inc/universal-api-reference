# CircleCI: Get Usage Export Job



```
GET https://connect.mindcloud.co/v1/universal/circleCI/latest/actions/get-usage-export-job
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CircleCI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/circleCI/latest/actions/get-usage-export-job?connectionId=$CONNECTION_ID&org_id=afbcafd1-31ea-4324-bc26-bf5d7e8e3e16" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "org_id": "afbcafd1-31ea-4324-bc26-bf5d7e8e3e16"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/circleCI/latest/actions/get-usage-export-job?${params}`, {
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
| `org_id` | string | yes | The CircleCI organization UUID. Default: `afbcafd1-31ea-4324-bc26-bf5d7e8e3e16`. |
| `usage_export_job_id` | string | no | The usage export job UUID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "downloadUrls": [
        "https://example.com"
      ],
      "errorReason": "string",
      "state": "string",
      "usageExportJobId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `downloadUrls` | array<string> |  |
| `errorReason` | string |  |
| `state` | string |  |
| `usageExportJobId` | string |  |

## Native endpoint

Through the native CircleCI API, this operation is `GET /organizations/:org_id/usage_export_job/:usage_export_job_id` (base URL `https://circleci.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-usage-export-job.md) for the provider-specific parameters and requirements.

