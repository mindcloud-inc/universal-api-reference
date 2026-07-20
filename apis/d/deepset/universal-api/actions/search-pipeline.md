# Deepset: Search Pipeline

Searches a Deepset pipeline with one or more queries.

```
GET https://connect.mindcloud.co/v1/universal/deepset/latest/actions/search-pipeline
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Deepset `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/deepset/latest/actions/search-pipeline?connectionId=$CONNECTION_ID&queries%5B%5D=string&workspaceName=Ava%20Chen&pipelineName=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "queries[]": "string",
  "workspaceName": "Ava Chen",
  "pipelineName": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/deepset/latest/actions/search-pipeline?${params}`, {
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
| `queries[]` | array<string> | yes | Queries to run through the deployed pipeline. |
| `workspaceName` | string | yes | deepset workspace name. |
| `pipelineName` | string | yes | deepset pipeline name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "results": [
        {
          "answers": [
            {
              "answer": "string",
              "type": "string"
            }
          ],
          "documents": [
            {
              "content": "string",
              "id": "string",
              "score": 1
            }
          ],
          "query": "string",
          "query_id": "string"
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
| `results[].answers[].answer` | string |  |
| `results[].answers[].type` | string |  |
| `results[].documents[].content` | string |  |
| `results[].documents[].id` | string |  |
| `results[].documents[].score` | number |  |
| `results[].query` | string |  |
| `results[].query_id` | string |  |

## Native endpoint

Through the native Deepset API, this operation is `POST /api/v1/workspaces/:workspace_name/pipelines/:pipeline_name/search` (base URL `https://api.cloud.deepset.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-pipeline.md) for the provider-specific parameters and requirements.

