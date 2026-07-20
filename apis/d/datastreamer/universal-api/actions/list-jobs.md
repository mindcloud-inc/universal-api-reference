# Datastreamer: List Jobs

Retrieves previously created jobs from Datastreamer.

```
GET https://connect.mindcloud.co/v1/universal/datastreamer/latest/actions/list-jobs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Datastreamer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/datastreamer/latest/actions/list-jobs?connectionId=$CONNECTION_ID&pipelineId=string&componentId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "pipelineId": "string",
  "componentId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/datastreamer/latest/actions/list-jobs?${params}`, {
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
| `pipelineId` | string | yes |  |
| `componentId` | string | yes |  |
| `count` | number | no | Default: `50`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Datastreamer API returns.

## Native endpoint

Through the native Datastreamer API, this operation is `GET /api/pipelines/:pipelineId/components/:componentId/jobs` (base URL `https://api.platform.datastreamer.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-jobs.md) for the provider-specific parameters and requirements.

