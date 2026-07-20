# Pinghome: Create Oncall Schedule

Creates a new on-call schedule in Pinghome.

```
POST https://connect.mindcloud.co/v1/universal/pinghome/latest/actions/create-oncall-schedule
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pinghome `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/pinghome/latest/actions/create-oncall-schedule" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "teamId": "string",
  "teamMemberId": "string",
  "startDate": "string",
  "endDate": "string",
  "monthsOfYear": "string",
  "weeksOfMonth": "string",
  "weekDays": "string",
  "startTime": "string",
  "endTime": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pinghome/latest/actions/create-oncall-schedule', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "teamId": "string",
    "teamMemberId": "string",
    "startDate": "string",
    "endDate": "string",
    "monthsOfYear": "string",
    "weeksOfMonth": "string",
    "weekDays": "string",
    "startTime": "string",
    "endTime": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `teamId` | string | yes | The team ID for the schedule. |
| `teamMemberId` | string | yes | The team member assigned to the schedule. |
| `startDate` | string | yes | The schedule start date in ISO-8601 format. |
| `endDate` | string | yes | The schedule end date in ISO-8601 format. |
| `monthsOfYear` | string<number> | yes | Months of the year included in the recurrence. |
| `weeksOfMonth` | string<number> | yes | Weeks of the month included in the recurrence. |
| `weekDays` | string<number> | yes | Weekdays included in the recurrence. |
| `startTime` | string | yes | The schedule start time in HH:mm:ss format. |
| `endTime` | string | yes | The schedule end time in HH:mm:ss format. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Pinghome API returns.

## Native endpoint

Through the native Pinghome API, this operation is `POST /incident-cmd/v1/team/:id/schedule` (base URL `https://api.pinghome.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-oncall-schedule.md) for the provider-specific parameters and requirements.

