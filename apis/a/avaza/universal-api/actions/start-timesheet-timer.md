# Avaza: Start Timesheet Timer

Starts a timesheet timer in Avaza.

```
PUT https://connect.mindcloud.co/v1/universal/avaza/latest/actions/start-timesheet-timer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Avaza `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/avaza/latest/actions/start-timesheet-timer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/avaza/latest/actions/start-timesheet-timer', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes | id of timesheet entry that should be used as the basis for running a timer. If the existing timesheet is not on the current day, or you have start/end times enabled, then a new timesheet will be created for the timer. |
| `userid` | number | no | Optional - User ID number if impersonating a different user. Otherwise assumes the current user. Only users with certain security roles have permission to impersonate other users |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Avaza API returns.

## Native endpoint

Through the native Avaza API, this operation is `POST /api/TimesheetTimer/:id` (base URL `https://api.avaza.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/start-timesheet-timer.md) for the provider-specific parameters and requirements.

