# 100Hires ATS: Update Job

Updates an existing job in 100Hires ATS.

```
PUT https://connect.mindcloud.co/v1/universal/hiresATS/latest/actions/update-job
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a 100Hires ATS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/hiresATS/latest/actions/update-job" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/hiresATS/latest/actions/update-job', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Job ID or alias to update. |
| `title` | string | no | Optional updated public job title. |
| `description` | string | no | Optional updated job description. |
| `status` | string | no | Optional updated job status. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `locationCity` | string | no | Optional updated job location city. |
| `locationCountry` | string | no | Optional updated job location country. |
| `workflowId` | number | no | Optional updated workflow ID. |
| `isRemote` | boolean | no | Optional remote flag. |
| `internalTitle` | string | no | Optional updated internal title. |
| `internalJobId` | string | no | Optional updated internal job identifier. |
| `include` | string | no | Optional comma-separated related job resources to include. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native 100Hires ATS API returns.

## Native endpoint

Through the native 100Hires ATS API, this operation is `PUT /jobs/:id` (base URL `https://api.100hires.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-job.md) for the provider-specific parameters and requirements.

