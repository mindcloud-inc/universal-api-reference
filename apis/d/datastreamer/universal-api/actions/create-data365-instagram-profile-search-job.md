# Datastreamer: Create Data365 Instagram Profile Search Job

Creates a Data365 Instagram profile search job in Datastreamer.

```
POST https://connect.mindcloud.co/v1/universal/datastreamer/latest/actions/create-data365-instagram-profile-search-job
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Datastreamer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/datastreamer/latest/actions/create-data365-instagram-profile-search-job" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/datastreamer/latest/actions/create-data365-instagram-profile-search-job', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `componentId` | string | no |  |
| `pipelineId` | string | no |  |
| `ready` | string | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Datastreamer API returns.

## Native endpoint

Through the native Datastreamer API, this operation is `POST /api/pipelines/:pipelineId/components/:componentId/jobs` (base URL `https://api.platform.datastreamer.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-data365-instagram-profile-search-job.md) for the provider-specific parameters and requirements.

