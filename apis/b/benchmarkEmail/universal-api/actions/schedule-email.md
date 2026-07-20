# Benchmark Email: Schedule Email

Schedules an email in Benchmark Email.

```
PUT https://connect.mindcloud.co/v1/universal/benchmarkEmail/latest/actions/schedule-email
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Benchmark Email `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/benchmarkEmail/latest/actions/schedule-email" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "scheduleDate": "string",
  "timeZone": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/benchmarkEmail/latest/actions/schedule-email', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "scheduleDate": "string",
    "timeZone": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Benchmark email ID. |
| `listId` | string | no | Optional resend target list ID. |
| `scheduleDate` | string | yes | Scheduled send datetime. |
| `sendType` | string | no | Optional resend send type. |
| `timeZone` | string | yes | Timezone for the scheduled send. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Benchmark Email API returns.

## Native endpoint

Through the native Benchmark Email API, this operation is `POST /Emails/:id/Schedule` (base URL `https://clientapi.benchmarkemail.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/schedule-email.md) for the provider-specific parameters and requirements.

