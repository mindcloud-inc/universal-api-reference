# Deepset: Get Pipeline Visualization

Retrieves visualization data for a Deepset pipeline.

```
GET https://connect.mindcloud.co/v1/universal/deepset/latest/actions/get-pipeline-visualization
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Deepset `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/deepset/latest/actions/get-pipeline-visualization?connectionId=$CONNECTION_ID&pipelineName=Ava%20Chen&workspaceName=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "pipelineName": "Ava Chen",
  "workspaceName": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/deepset/latest/actions/get-pipeline-visualization?${params}`, {
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
      "edges": [
        {
          "source": "string",
          "target": "string"
        }
      ],
      "nodes": [
        {
          "id": "string",
          "label": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `edges[].source` | string |  |
| `edges[].target` | string |  |
| `nodes[].id` | string |  |
| `nodes[].label` | string |  |

## Native endpoint

Through the native Deepset API, this operation is `GET /api/v1/workspaces/:workspace_name/pipelines/:pipeline_name/visualization` (base URL `https://api.cloud.deepset.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-pipeline-visualization.md) for the provider-specific parameters and requirements.

