# Dremio: Get Job

Retrieves a job from a Dremio project.

```
GET https://connect.mindcloud.co/v1/universal/dremio/latest/actions/get-job
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dremio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dremio/latest/actions/get-job?connectionId=$CONNECTION_ID&id=string&projectId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string",
  "projectId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dremio/latest/actions/get-job?${params}`, {
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
| `id` | string | yes |  |
| `projectId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "cancellationReason": "string",
      "endedAt": "string",
      "errorMessage": "string",
      "jobState": "string",
      "queryType": "string",
      "rowCount": 1,
      "startedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cancellationReason` | string |  |
| `endedAt` | string |  |
| `errorMessage` | string |  |
| `jobState` | string |  |
| `queryType` | string |  |
| `rowCount` | number |  |
| `startedAt` | string |  |

## Native endpoint

Through the native Dremio API, this operation is `GET /projects/:project_id/job/:id` (base URL `https://api.dremio.cloud/v0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-job.md) for the provider-specific parameters and requirements.

