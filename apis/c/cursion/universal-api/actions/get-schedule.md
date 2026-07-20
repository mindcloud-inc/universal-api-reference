# Cursion: Get Schedule

Retrieves an existing schedule from Cursion.

```
GET https://connect.mindcloud.co/v1/universal/cursion/latest/actions/get-schedule
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cursion `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cursion/latest/actions/get-schedule?connectionId=$CONNECTION_ID&scheduleId=placeholder-schedule-id" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "scheduleId": "placeholder-schedule-id"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cursion/latest/actions/get-schedule?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `scheduleId` | string | yes | The schedule identifier. Default: `placeholder-schedule-id`. |

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

Through the native Cursion API, this operation is `GET /schedule/{{scheduleId}}` (base URL `https://api.cursion.dev/v1/ops`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-schedule.md) for the provider-specific parameters and requirements.

