# Avaza: Update Timesheet

Updates an existing timesheet in Avaza.

```
PUT https://connect.mindcloud.co/v1/universal/avaza/latest/actions/update-timesheet
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Avaza `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/avaza/latest/actions/update-timesheet" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "timesheetentryid": 1,
  "fieldstoupdate": "string",
  "projectidfk": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/avaza/latest/actions/update-timesheet', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "timesheetentryid": 1,
    "fieldstoupdate": "string",
    "projectidfk": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `timesheetentryid` | number | yes |  |
| `fieldstoupdate` | list<string> | yes |  |
| `projectidfk` | number | yes |  |
| `timesheetcategoryidfk` | number | no |  |
| `taskidfk` | number | no |  |
| `duration` | number | no |  |
| `entrydate` | date | no |  |
| `hasstartendtime` | boolean | no |  |
| `notes` | string | no |  |
| `custommetadata` | string | no | Optional. free nvarchar field available via Api to store any additional metadata against a timesheet. We suggest you use Json or your preferred serialisation format. 1000 characters max. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Avaza API returns.

## Native endpoint

Through the native Avaza API, this operation is `PUT /api/Timesheet` (base URL `https://api.avaza.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-timesheet.md) for the provider-specific parameters and requirements.

