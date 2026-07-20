# Avaza: Submit Timesheets for Approval

Submits timesheets for approval in Avaza.

```
PUT https://connect.mindcloud.co/v1/universal/avaza/latest/actions/submit-timesheets-for-approval
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Avaza `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/avaza/latest/actions/submit-timesheets-for-approval" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/avaza/latest/actions/submit-timesheets-for-approval', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `sendnotifications` | boolean | no | Send email alerts to timesheet approvers. Defaults to true |
| `wholeweekof` | date | no | A date (yyyy-MM-dd) that falls within a Week to have all timesheets in that week submitted. Respects the First Day of Week setting in your account Timesheet Settings to determine the week range. |
| `wholedayof` | date | no | A date (yyyy-MM-dd) to submit all timesheets on this day |
| `userid` | number | no | The user to submit timesheets for. Defaults to current user. Only allowed to be different from the current user when the current user has rights to Impersonate other users. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Avaza API returns.

## Native endpoint

Through the native Avaza API, this operation is `POST /api/TimesheetSubmission` (base URL `https://api.avaza.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/submit-timesheets-for-approval.md) for the provider-specific parameters and requirements.

