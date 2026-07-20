# Seqera: List Pipeline Versions

Retrieves pipeline versions from Seqera.

```
GET https://connect.mindcloud.co/v1/universal/seqera/latest/actions/list-pipeline-versions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Seqera `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/seqera/latest/actions/list-pipeline-versions?connectionId=$CONNECTION_ID&pipelineId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "pipelineId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/seqera/latest/actions/list-pipeline-versions?${params}`, {
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
| `isPublished` | boolean | no |  |
| `max` | number | no |  |
| `offset` | number | no |  |
| `pipelineId` | number | yes |  |
| `search` | string | no |  |
| `workspaceId` | number | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Seqera API returns.

## Native endpoint

Through the native Seqera API, this operation is `GET /pipelines/:pipelineId/versions` (base URL `https://api.cloud.seqera.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-pipeline-versions.md) for the provider-specific parameters and requirements.

