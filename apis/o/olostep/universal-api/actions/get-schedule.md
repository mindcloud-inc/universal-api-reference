# Olostep: Get Schedule

Retrieves details for a schedule in Olostep.

```
GET https://connect.mindcloud.co/v1/universal/olostep/latest/actions/get-schedule
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Olostep `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/olostep/latest/actions/get-schedule?connectionId=$CONNECTION_ID&scheduleId=schedule_123" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "scheduleId": "schedule_123"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/olostep/latest/actions/get-schedule?${params}`, {
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
| `scheduleId` | string | yes | Unique schedule identifier. Olostep schedule IDs start with `schedule_`. Example: `schedule_123`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "cronExpression": "string",
      "endpoint": "string",
      "expressionTimezone": "string",
      "method": "string",
      "payload": {
        "retrieveId": "string"
      },
      "scheduleGroup": "string",
      "scheduleId": "string",
      "scheduleName": "Ava Chen",
      "state": "string",
      "teamId": "string",
      "text": "string",
      "type": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `cronExpression` | string |  |
| `endpoint` | string |  |
| `expressionTimezone` | string |  |
| `method` | string |  |
| `payload.retrieveId` | string |  |
| `scheduleGroup` | string |  |
| `scheduleId` | string |  |
| `scheduleName` | string |  |
| `state` | string |  |
| `teamId` | string |  |
| `text` | string |  |
| `type` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Olostep API, this operation is `GET /v1/schedules/[:schedule_id]` (base URL `https://api.olostep.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-schedule.md) for the provider-specific parameters and requirements.

