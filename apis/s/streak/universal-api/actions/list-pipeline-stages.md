# Streak: List Pipeline Stages

Retrieves pipeline stages from Streak.

```
GET https://connect.mindcloud.co/v1/universal/streak/latest/actions/list-pipeline-stages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Streak `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/streak/latest/actions/list-pipeline-stages?connectionId=$CONNECTION_ID&pipelineKey=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "pipelineKey": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/streak/latest/actions/list-pipeline-stages?${params}`, {
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
| `pipelineKey` | string | yes | Pipeline key for the pipeline whose stages you want to list. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Streak API returns.

## Native endpoint

Through the native Streak API, this operation is `GET /api/v1/pipelines/:pipelineKey/stages` (base URL `https://api.streak.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-pipeline-stages.md) for the provider-specific parameters and requirements.

