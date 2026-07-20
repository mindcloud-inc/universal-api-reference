# Deepset: Get Pipeline Stats

Retrieves statistics for a Deepset pipeline.

```
GET https://connect.mindcloud.co/v1/universal/deepset/latest/actions/get-pipeline-stats
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Deepset `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/deepset/latest/actions/get-pipeline-stats?connectionId=$CONNECTION_ID&pipelineName=Ava%20Chen&workspaceName=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "pipelineName": "Ava Chen",
  "workspaceName": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/deepset/latest/actions/get-pipeline-stats?${params}`, {
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
| `pipelineName` | string | yes | deepset pipeline name. |
| `workspaceName` | string | yes | deepset workspace name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "errors": 1,
      "latency": 1,
      "requests": 1,
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `errors` | number |  |
| `latency` | number |  |
| `requests` | number |  |
| `status` | string |  |

## Native endpoint

Through the native Deepset API, this operation is `GET /api/v1/workspaces/:workspace_name/pipelines/:pipeline_name/stats` (base URL `https://api.cloud.deepset.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-pipeline-stats.md) for the provider-specific parameters and requirements.

