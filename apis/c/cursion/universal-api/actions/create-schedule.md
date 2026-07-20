# Cursion: Create Schedule



```
POST https://connect.mindcloud.co/v1/universal/cursion/latest/actions/create-schedule
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cursion `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/cursion/latest/actions/create-schedule" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "beginDate": "string",
  "frequency": "string",
  "siteId": "string",
  "taskType": "string",
  "time": "string",
  "timezone": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cursion/latest/actions/create-schedule', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "beginDate": "string",
    "frequency": "string",
    "siteId": "string",
    "taskType": "string",
    "time": "string",
    "timezone": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `beginDate` | string | yes | The date to start the schedule. |
| `frequency` | string | yes | How often the schedule runs. |
| `siteId` | string | yes | The site identifier to schedule. |
| `taskType` | string | yes | The scheduled task type: scan, test, or report. |
| `time` | string | yes | The 24-hour time to run the schedule. |
| `timezone` | string | yes | The IANA timezone for the schedule. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "alert": "string",
      "begin_date": "string",
      "crontab_id": "string",
      "extras": {},
      "frequency": "string",
      "id": "string",
      "page": "string",
      "periodic_task_id": "string",
      "site": "string",
      "status": "string",
      "task": "string",
      "task_type": "string",
      "time": "string",
      "time_created": "string",
      "timezone": "string",
      "user": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `alert` | string |  |
| `begin_date` | string |  |
| `crontab_id` | string |  |
| `extras` | object |  |
| `frequency` | string |  |
| `id` | string |  |
| `page` | string |  |
| `periodic_task_id` | string |  |
| `site` | string |  |
| `status` | string |  |
| `task` | string |  |
| `task_type` | string |  |
| `time` | string |  |
| `time_created` | string |  |
| `timezone` | string |  |
| `user` | string |  |

## Native endpoint

Through the native Cursion API, this operation is `POST /schedule` (base URL `https://api.cursion.dev/v1/ops`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-schedule.md) for the provider-specific parameters and requirements.

