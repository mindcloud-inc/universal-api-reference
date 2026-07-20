# Avaza: Create Timesheet

Creates a new timesheet in Avaza.

```
POST https://connect.mindcloud.co/v1/universal/avaza/latest/actions/create-timesheet
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Avaza `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/avaza/latest/actions/create-timesheet" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/avaza/latest/actions/create-timesheet', {
  method: 'POST',
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
| `useridfk` | number | no | UserID for a Timesheet user in Avaza |
| `projectidfk` | number | no | The project to associate the timesheet with. |
| `timesheetcategoryidfk` | number | no | The Project timesheet category to link the timesheet to |
| `duration` | number | no | The duration of the timesheet, in decimal hours. If null or 0, a timer will be started. |
| `isinvoiced` | boolean | no | Optional. False by default. Allows you to mark the timesheet as invoiced in an external system. |
| `entrydate` | date | no | The date of the timesheet entry, with an optional start time component. |
| `hasstartendtime` | boolean | no | If true, the start time will be take from the time component of the Entry Date field, and the end time will be calculated by adding the Duration to the StartDate |
| `notes` | string | no | Timesheet Notes |
| `taskidfk` | number | no | Optional. Link the timesheet to a specific task |
| `custommetadata` | string | no | Optional. free nvarchar field available via Api to store any additional metadata against a timesheet. We suggest you use Json or your preferred serialisation format. 1000 characters max. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Avaza API returns.

## Native endpoint

Through the native Avaza API, this operation is `POST /api/Timesheet` (base URL `https://api.avaza.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-timesheet.md) for the provider-specific parameters and requirements.

