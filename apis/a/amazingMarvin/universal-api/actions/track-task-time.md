# Amazing Marvin: Track Task Time

Starts or stops task time tracking in Amazing Marvin.

```
PUT https://connect.mindcloud.co/v1/universal/amazingMarvin/latest/actions/track-task-time
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Amazing Marvin `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/amazingMarvin/latest/actions/track-task-time" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "taskId": "string",
  "action": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/amazingMarvin/latest/actions/track-task-time', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "taskId": "string",
    "action": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `taskId` | string | yes | Task ID to track. |
| `action` | string | yes | START or STOP. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "issues": {},
      "startId": "string",
      "startTimes": {},
      "stopId": "string",
      "stopTimes": [
        [
          "2026-05-07T12:00:00.000Z"
        ]
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `issues` | object |  |
| `startId` | string |  |
| `startTimes` | object |  |
| `stopId` | string |  |
| `stopTimes[]` | array<date> |  |

## Native endpoint

Through the native Amazing Marvin API, this operation is `POST /track` (base URL `https://serv.amazingmarvin.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/track-task-time.md) for the provider-specific parameters and requirements.

