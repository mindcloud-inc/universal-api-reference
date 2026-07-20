# Pinghome: Update Oncall Schedule

Updates an existing on-call schedule in Pinghome.

```
PUT https://connect.mindcloud.co/v1/universal/pinghome/latest/actions/update-oncall-schedule
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pinghome `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/pinghome/latest/actions/update-oncall-schedule" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "teamId": "string",
  "teamMemberId": "string",
  "createdAt": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pinghome/latest/actions/update-oncall-schedule', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "teamId": "string",
    "teamMemberId": "string",
    "createdAt": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `teamId` | string | yes | The unique ID of the team. |
| `teamMemberId` | string | yes | The unique ID of the team member assigned to the schedule. |
| `createdAt` | string | yes | The creation timestamp identifying the schedule. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `startDate` | string | no | The schedule start date in ISO-8601 format. |
| `endDate` | string | no | The schedule end date in ISO-8601 format. |
| `monthsOfYear` | string | no | Months of the year included in the recurrence. |
| `weeksOfMonth` | string | no | Weeks of the month included in the recurrence. |
| `weekDays` | string | no | Weekdays included in the recurrence. |
| `startTime` | string | no | The schedule start time in HH:mm:ss format. |
| `endTime` | string | no | The schedule end time in HH:mm:ss format. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Pinghome API returns.

## Native endpoint

Through the native Pinghome API, this operation is `PUT /incident-cmd/v1/team/:id/schedule` (base URL `https://api.pinghome.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-oncall-schedule.md) for the provider-specific parameters and requirements.

