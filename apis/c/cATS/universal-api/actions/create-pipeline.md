# CATS: Create Pipeline

Creates a new pipeline in CATS.

```
POST https://connect.mindcloud.co/v1/universal/cATS/latest/actions/create-pipeline
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CATS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/cATS/latest/actions/create-pipeline" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "candidateId": "411876208",
  "jobId": "16789175"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cATS/latest/actions/create-pipeline', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "candidateId": "411876208",
    "jobId": "16789175"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `candidateId` | number | yes | The candidate ID for the pipeline. Example: `411876208`. |
| `jobId` | number | yes | The job ID for the pipeline. Example: `16789175`. |
| `rating` | number | no | The candidate rating for the job. Example: `3`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native CATS API returns.

## Native endpoint

Through the native CATS API, this operation is `POST /pipelines` (base URL `https://api.catsone.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-pipeline.md) for the provider-specific parameters and requirements.

