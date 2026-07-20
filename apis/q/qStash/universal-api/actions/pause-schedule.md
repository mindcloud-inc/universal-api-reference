# QStash: Pause Schedule

Pauses an existing schedule in QStash.

```
PUT https://connect.mindcloud.co/v1/universal/qStash/latest/actions/pause-schedule
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a QStash `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/qStash/latest/actions/pause-schedule" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "scheduleId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/qStash/latest/actions/pause-schedule', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "scheduleId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `scheduleId` | string | yes | Identifier of the schedule to pause. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native QStash API returns.

## Native endpoint

Through the native QStash API, this operation is `POST /v2/schedules/:scheduleId/pause` (base URL `https://qstash-eu-central-1.upstash.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/pause-schedule.md) for the provider-specific parameters and requirements.

