# Olostep: Delete Schedule

Deletes an existing schedule from Olostep.

```
DELETE https://connect.mindcloud.co/v1/universal/olostep/latest/actions/delete-schedule
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Olostep `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/olostep/latest/actions/delete-schedule?connectionId=$CONNECTION_ID&scheduleId=schedule_123" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "scheduleId": "schedule_123"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/olostep/latest/actions/delete-schedule?${params}`, {
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
| `scheduleId` | string | yes | Unique identifier for the schedule to delete. Must start with `schedule_`. Example: `schedule_123`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "scheduleId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string |  |
| `scheduleId` | string |  |

## Native endpoint

Through the native Olostep API, this operation is `DELETE /v1/schedules/[:schedule_id]` (base URL `https://api.olostep.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-schedule.md) for the provider-specific parameters and requirements.

