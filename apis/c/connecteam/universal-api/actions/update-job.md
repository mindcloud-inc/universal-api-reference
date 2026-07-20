# Connecteam: Update Job

Update a single job by its unique identifier. Currently, updating job with nested sub-jobs is not supported.

```
PUT https://connect.mindcloud.co/v1/universal/connecteam/latest/actions/update-job
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Connecteam `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/connecteam/latest/actions/update-job" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "jobId": "string",
  "title": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/connecteam/latest/actions/update-job', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "jobId": "string",
    "title": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `jobId` | string | yes |  |
| `title` | string | yes |  |
| `code` | string | no |  |
| `description` | string | no |  |
| `gps` | object | no |  |
| `gps.address` | string | no |  |
| `gps.longitude` | number | no |  |
| `gps.latitude` | number | no |  |
| `assign` | object | no |  |
| `assign.type` | string | no | Default: `both`. |
| `assign.userIds[]` | array<number> | no |  |
| `assign.groupIds[]` | array<number> | no |  |
| `customFields[]` | array<object> | no |  |
| `customFields[].customFieldId` | number | no |  |
| `customFields[].value` | string | no |  |
| `parentId` | string | no |  |
| `useParentData` | boolean | no |  |

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
| `title` | string |  |
| `useParentData` | boolean |  |

## Native endpoint

Through the native Connecteam API, this operation is `PUT /jobs/v1/jobs/:jobId` (base URL `https://api.connecteam.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-job.md) for the provider-specific parameters and requirements.

