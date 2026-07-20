# Honeybadger: Report Check-in Details

Reports check-in details to Honeybadger by ID.

```
POST https://connect.mindcloud.co/v1/universal/honeybadger/latest/actions/report-check-in-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Honeybadger `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/honeybadger/latest/actions/report-check-in-details" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "checkInId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/honeybadger/latest/actions/report-check-in-details', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "checkInId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `checkInId` | string | yes | The case-sensitive check-in endpoint ID from Honeybadger. |
| `checkIn.status` | string | no | Check-in result status: success or error. |
| `checkIn.duration` | number | no | Execution duration in milliseconds. |
| `checkIn.stdout` | string | no | Captured standard output. |
| `checkIn.stderr` | string | no | Captured standard error. |
| `checkIn.exitCode` | number | no | Process exit code. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Honeybadger API returns.

## Native endpoint

Through the native Honeybadger API, this operation is `POST /check_in/:checkInId` (base URL `https://api.honeybadger.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/report-check-in-details.md) for the provider-specific parameters and requirements.

