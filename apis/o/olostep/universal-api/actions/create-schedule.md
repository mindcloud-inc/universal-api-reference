# Olostep: Create Schedule

Creates a new schedule in Olostep.

```
POST https://connect.mindcloud.co/v1/universal/olostep/latest/actions/create-schedule
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Olostep `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/olostep/latest/actions/create-schedule" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "method": "GET",
  "endpoint": "/v1/scrapes"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/olostep/latest/actions/create-schedule', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "method": "GET",
    "endpoint": "/v1/scrapes"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `method` | string | yes | HTTP method the schedule should use when calling the Olostep endpoint. One of: `0`, `1`. Example: `GET`. |
| `endpoint` | string | yes | Olostep API endpoint path to call, such as `/v1/retrieve` or `/v1/searches`. Example: `/v1/scrapes`. |
| `payload` | object | no | JSON payload to send when the scheduled request runs. Example: `[object Object]`. |
| `cronExpression` | string | no | Cron expression for a recurring schedule. Example: `0 9 * * MON-FRI`. |
| `executeAt` | date | no | One-time execution timestamp in ISO 8601 format. Example: `2026-03-24T15:00:00Z`. |
| `expressionTimezone` | string | no | Timezone used when interpreting the cron expression. Example: `America/New_York`. |
| `text` | string | no | Natural-language schedule text for Olostep to interpret. Example: `every weekday at 9am Eastern`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created": "2026-05-07T12:00:00.000Z",
      "cronExpression": "string",
      "endpoint": "string",
      "expressionTimezone": "string",
      "id": "string",
      "method": "string",
      "object": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created` | date |  |
| `cronExpression` | string |  |
| `endpoint` | string |  |
| `expressionTimezone` | string |  |
| `id` | string |  |
| `method` | string |  |
| `object` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Olostep API, this operation is `POST /v1/schedules` (base URL `https://api.olostep.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-schedule.md) for the provider-specific parameters and requirements.

