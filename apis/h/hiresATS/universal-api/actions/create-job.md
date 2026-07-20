# 100Hires ATS: Create Job

Creates a new job in 100Hires ATS.

```
POST https://connect.mindcloud.co/v1/universal/hiresATS/latest/actions/create-job
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a 100Hires ATS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/hiresATS/latest/actions/create-job" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "companyId": 1,
  "status": "string",
  "title": "string",
  "description": "string",
  "locationCity": "string",
  "locationCountry": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/hiresATS/latest/actions/create-job', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "companyId": 1,
    "status": "string",
    "title": "string",
    "description": "string",
    "locationCity": "string",
    "locationCountry": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `companyId` | number | yes | Company ID that owns the job. |
| `status` | string | yes | Initial job status name. |
| `title` | string | yes | Public job title. |
| `description` | string | yes | Job description in HTML or text. |
| `locationCity` | string | yes | Job location city. |
| `locationCountry` | string | yes | Job location country. |
| `workflowId` | number | no | Optional workflow ID to apply to the job. |
| `isRemote` | boolean | no | Whether the job is remote. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `internalTitle` | string | no | Optional internal-only job title. |
| `internalJobId` | string | no | Optional internal identifier for the job. |
| `include` | string | no | Optional comma-separated related job resources to include. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native 100Hires ATS API returns.

## Native endpoint

Through the native 100Hires ATS API, this operation is `POST /jobs` (base URL `https://api.100hires.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-job.md) for the provider-specific parameters and requirements.

