# Connecteam: Create Jobs

Create individual or multiple jobs under a specified scheduler

```
POST https://connect.mindcloud.co/v1/universal/connecteam/latest/actions/create-jobs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Connecteam `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/connecteam/latest/actions/create-jobs" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "jobs[].instanceIds[]": [
    1
  ],
  "jobs[].title": "string",
  "jobs[].subJobs[].title": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/connecteam/latest/actions/create-jobs', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "jobs[].instanceIds[]": [1],
    "jobs[].title": "string",
    "jobs[].subJobs[].title": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `jobs[]` | array<object> | no |  |
| `jobs[].instanceIds[]` | array<number> | yes |  |
| `jobs[].title` | string | yes |  |
| `jobs[].code` | string | no |  |
| `jobs[].description` | string | no |  |
| `jobs[].gps` | object | no |  |
| `jobs[].gps.address` | string | no |  |
| `jobs[].gps.longitude` | number | no |  |
| `jobs[].gps.latitude` | number | no |  |
| `jobs[].assign` | object | no |  |
| `jobs[].assign.type` | string | no | Default: `both`. |
| `jobs[].assign.userIds[]` | array<number> | no |  |
| `jobs[].assign.groupIds[]` | array<number> | no |  |
| `jobs[].customFields[]` | array<object> | no |  |
| `jobs[].customFields[].customFieldId` | number | no |  |
| `jobs[].customFields[].value` | string | no |  |
| `jobs[].color` | string | no |  |
| `jobs[].subJobs[]` | array<object> | no |  |
| `jobs[].subJobs[].title` | string | yes |  |
| `jobs[].subJobs[].code` | string | no |  |
| `jobs[].subJobs[].description` | string | no |  |
| `jobs[].subJobs[].gps` | object | no |  |
| `jobs[].subJobs[].gps.address` | string | no |  |
| `jobs[].subJobs[].gps.longitude` | number | no |  |
| `jobs[].subJobs[].gps.latitude` | number | no |  |
| `jobs[].subJobs[].assign` | object | no |  |
| `jobs[].subJobs[].assign.type` | string | no | Default: `both`. |
| `jobs[].subJobs[].assign.userIds[]` | array<number> | no |  |
| `jobs[].subJobs[].assign.groupIds[]` | array<number> | no |  |
| `jobs[].subJobs[].customFields[]` | array<object> | no |  |
| `jobs[].subJobs[].customFields[].customFieldId` | number | no |  |
| `jobs[].subJobs[].customFields[].value` | string | no |  |
| `jobs[].subJobs[].useParentData` | boolean | no | Default: `true`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "assign": {
        "type": "string"
      },
      "code": "string",
      "color": "string",
      "description": "string",
      "gps": {
        "address": "string"
      },
      "instanceIds": [
        1
      ],
      "isDeleted": true,
      "jobId": "string",
      "subJobs": [
        {
          "assign": {
            "type": "string"
          },
          "code": "string",
          "color": "string",
          "description": "string",
          "gps": {
            "address": "string"
          },
          "isDeleted": true,
          "jobId": "string",
          "parentId": "string",
          "title": "string",
          "useParentData": true
        }
      ],
      "title": "string",
      "useParentData": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `assign.type` | string |  |
| `code` | string |  |
| `color` | string |  |
| `description` | string |  |
| `gps.address` | string |  |
| `instanceIds[]` | number |  |
| `isDeleted` | boolean |  |
| `jobId` | string |  |
| `subJobs[].assign.type` | string |  |
| `subJobs[].code` | string |  |
| `subJobs[].color` | string |  |
| `subJobs[].description` | string |  |
| `subJobs[].gps.address` | string |  |
| `subJobs[].isDeleted` | boolean |  |
| `subJobs[].jobId` | string |  |
| `subJobs[].parentId` | string |  |
| `subJobs[].title` | string |  |
| `subJobs[].useParentData` | boolean |  |
| `title` | string |  |
| `useParentData` | boolean |  |

## Native endpoint

Through the native Connecteam API, this operation is `POST /jobs/v1/jobs` (base URL `https://api.connecteam.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-jobs.md) for the provider-specific parameters and requirements.

