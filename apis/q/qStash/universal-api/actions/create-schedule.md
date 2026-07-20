# QStash: Create Schedule

Creates a recurring delivery schedule in QStash.

```
POST https://connect.mindcloud.co/v1/universal/qStash/latest/actions/create-schedule
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a QStash `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/qStash/latest/actions/create-schedule" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "destination": "string",
  "cron": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/qStash/latest/actions/create-schedule', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "destination": "string",
    "cron": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `destination` | string | yes | Destination URL or URL Group name. |
| `cron` | string | yes | Cron expression for the schedule. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "scheduleId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `scheduleId` | string |  |

## Native endpoint

Through the native QStash API, this operation is `POST /v2/schedules/:destination` (base URL `https://qstash-eu-central-1.upstash.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-schedule.md) for the provider-specific parameters and requirements.

