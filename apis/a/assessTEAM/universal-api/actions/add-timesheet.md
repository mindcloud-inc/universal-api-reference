# AssessTEAM: Add Timesheet

Creates a new timesheet entry in AssessTEAM.

```
POST https://connect.mindcloud.co/v1/universal/assessTEAM/latest/actions/add-timesheet
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AssessTEAM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/assessTEAM/latest/actions/add-timesheet" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "projectName": "Ava Chen",
  "personCode": "string",
  "timeBy": "Time_by_Month",
  "dateOrMonth": "string",
  "hours": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/assessTEAM/latest/actions/add-timesheet', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "projectName": "Ava Chen",
    "personCode": "string",
    "timeBy": "Time_by_Month",
    "dateOrMonth": "string",
    "hours": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `projectName` | string | yes | Project name, for example Acme Sample Project. |
| `personCode` | string | yes | Unique person code, for example 1001. |
| `timeBy` | string | yes | Time by mode, either Time_by_Day or Time_by_Month. Default: `Time_by_Month`. |
| `dateOrMonth` | string | yes | Date for day mode or month for month mode, for example Apr-2026. |
| `hours` | number | yes | Hours, for example 8.5. |
| `comment` | string | no | Optional comment for the timesheet entry. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "result": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `result` | string |  |

## Native endpoint

Through the native AssessTEAM API, this operation is `POST /timesheet/addtimesheet` (base URL `https://restapi.assessteam.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-timesheet.md) for the provider-specific parameters and requirements.

