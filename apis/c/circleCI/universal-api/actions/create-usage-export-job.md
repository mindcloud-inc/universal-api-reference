# CircleCI: Create Usage Export Job



```
POST https://connect.mindcloud.co/v1/universal/circleCI/latest/actions/create-usage-export-job
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CircleCI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/circleCI/latest/actions/create-usage-export-job" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "end": "2026-04-07T23:59:59Z",
  "org_id": "afbcafd1-31ea-4324-bc26-bf5d7e8e3e16",
  "start": "2026-04-01T00:00:00Z"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/circleCI/latest/actions/create-usage-export-job', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "end": "2026-04-07T23:59:59Z",
    "org_id": "afbcafd1-31ea-4324-bc26-bf5d7e8e3e16",
    "start": "2026-04-01T00:00:00Z"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `end` | string | yes | The inclusive end date-time for the usage export. Default: `2026-04-07T23:59:59Z`. |
| `org_id` | string | yes | The CircleCI organization UUID. Default: `afbcafd1-31ea-4324-bc26-bf5d7e8e3e16`. |
| `start` | string | yes | The inclusive start date-time for the usage export. Default: `2026-04-01T00:00:00Z`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "downloadUrls": [
        "https://example.com"
      ],
      "end": "string",
      "start": "string",
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
| `end` | string |  |
| `start` | string |  |
| `state` | string |  |
| `usageExportJobId` | string |  |

## Native endpoint

Through the native CircleCI API, this operation is `POST /organizations/:org_id/usage_export_job` (base URL `https://circleci.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-usage-export-job.md) for the provider-specific parameters and requirements.

