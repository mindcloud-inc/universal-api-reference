# Streamtime: Update Job Status



```
PUT https://connect.mindcloud.co/v1/universal/streamtime/latest/actions/update-job-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Streamtime `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/streamtime/latest/actions/update-job-status" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "jobId": "601",
  "jobStatusId": "1"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/streamtime/latest/actions/update-job-status', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "jobId": "601",
    "jobStatusId": "1"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `jobId` | number | yes | Job ID Example: `601`. |
| `jobStatusId` | number | yes | Job Status ID (5=Paused, 1=In Play, 2=Done, 3=Deleted, 4=Archived) Example: `1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "modelSet": [
        "string"
      ],
      "primaryModel": {},
      "primaryModelClassName": "Ava Chen",
      "removedEntityIds": [
        "string"
      ],
      "syncKeyReplacementSet": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `modelSet` | array |  |
| `primaryModel` | object |  |
| `primaryModelClassName` | string |  |
| `removedEntityIds` | array |  |
| `syncKeyReplacementSet` | object |  |

## Native endpoint

Through the native Streamtime API, this operation is `PUT /jobs/:job_id/job_status` (base URL `https://api.streamtime.net/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-job-status.md) for the provider-specific parameters and requirements.

