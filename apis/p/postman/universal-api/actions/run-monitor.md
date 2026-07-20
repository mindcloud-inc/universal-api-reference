# Postman: Run Monitor

Runs an existing monitor in Postman.

```
POST https://connect.mindcloud.co/v1/universal/postman/latest/actions/run-monitor
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Postman `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/postman/latest/actions/run-monitor" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "monitorId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/postman/latest/actions/run-monitor', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "monitorId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `monitorId` | string | yes | The monitor's ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "run": {
        "executions": [
          {
            "id": 1,
            "request": {
              "method": "string"
            },
            "response": {
              "code": 1
            }
          }
        ],
        "info": {
          "finishedAt": "2026-05-07T12:00:00.000Z",
          "jobId": "string",
          "monitorId": "string",
          "name": "Ava Chen",
          "startedAt": "2026-05-07T12:00:00.000Z",
          "status": "string"
        },
        "stats": {
          "errorCount": 1,
          "runCount": 1
        }
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `run.executions[].id` | number |  |
| `run.executions[].request.method` | string |  |
| `run.executions[].response.code` | number |  |
| `run.info.finishedAt` | date |  |
| `run.info.jobId` | string |  |
| `run.info.monitorId` | string |  |
| `run.info.name` | string |  |
| `run.info.startedAt` | date |  |
| `run.info.status` | string |  |
| `run.stats.errorCount` | number |  |
| `run.stats.runCount` | number |  |

## Native endpoint

Through the native Postman API, this operation is `POST /monitors/:monitorId/run` (base URL `https://api.getpostman.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/run-monitor.md) for the provider-specific parameters and requirements.

