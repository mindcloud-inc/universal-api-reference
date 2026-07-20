# Wodely: Assign Tasks to Driver in Batch



```
PUT https://connect.mindcloud.co/v1/universal/wodely/latest/actions/assign-tasks-to-driver-in-batch
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Wodely `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/wodely/latest/actions/assign-tasks-to-driver-in-batch" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "assignments[].taskGuid": "DD2A6408A6",
  "assignments[].driverUserId": "driver@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/wodely/latest/actions/assign-tasks-to-driver-in-batch', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "assignments[].taskGuid": "DD2A6408A6",
    "assignments[].driverUserId": "driver@example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `assignments[].taskGuid` | string | yes | Task Id. Example: `DD2A6408A6`. |
| `assignments[].driverUserId` | string | yes | Driver user id, username, or email. Example: `driver@example.com`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": "string",
      "message": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | string |  |
| `message` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native Wodely API, this operation is `POST /v2/tasks/driver` (base URL `https://api.wodely.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/assign-tasks-to-driver-in-batch.md) for the provider-specific parameters and requirements.

