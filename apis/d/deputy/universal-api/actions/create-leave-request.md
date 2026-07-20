# Deputy: Create Leave Request

Creates a new leave request in Deputy.

```
POST https://connect.mindcloud.co/v1/universal/deputy/latest/actions/create-leave-request
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Deputy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/deputy/latest/actions/create-leave-request" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "Employee": 1,
  "LeaveRule": 1,
  "Company": 1,
  "DateStart": "2026-03-19",
  "Start": 1,
  "DateEnd": "2026-03-19",
  "End": 1,
  "Comment": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/deputy/latest/actions/create-leave-request', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "Employee": 1,
    "LeaveRule": 1,
    "Company": 1,
    "DateStart": "2026-03-19",
    "Start": 1,
    "DateEnd": "2026-03-19",
    "End": 1,
    "Comment": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `Employee` | number | yes | The id record number of the employee who is requesting leave. |
| `LeaveRule` | number | yes | The id record number of the Leave Rule being included. |
| `Company` | number | yes | The location which the leave application is being applied against. |
| `DateStart` | string | yes | The start date of the leave in YYYY-MM-DD format. Example: `2026-03-19`. |
| `Start` | number | yes | The start time of the leave in unix timestamp format. |
| `DateEnd` | string | yes | The end date of the leave in YYYY-MM-DD format. Example: `2026-03-19`. |
| `End` | number | yes | The end time of the leave in unix timestamp format. |
| `Comment` | string | yes | A comment explaining the leave to the manager from the employee. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "allDay": true,
      "approvalComment": "string",
      "approverPay": 1,
      "approverTime": 1,
      "comment": "string",
      "company": 1,
      "created": "2026-05-07T12:00:00.000Z",
      "creator": 1,
      "dateEnd": "2026-05-07T12:00:00.000Z",
      "dateEndAllDay": true,
      "dateStart": "2026-05-07T12:00:00.000Z",
      "dateStartAllDay": true,
      "days": 1,
      "DPMetaData": {},
      "employee": 1,
      "employeeHistory": 1,
      "employeeName": "Ava Chen",
      "end": 1,
      "endTimeLocalized": "2026-05-07T12:00:00.000Z",
      "externalId": 1,
      "id": 1,
      "leavePayLineArray": [
        "string"
      ],
      "leaveRule": 1,
      "modified": "2026-05-07T12:00:00.000Z",
      "notifyManagerArray": [
        "string"
      ],
      "start": 1,
      "startTimeLocalized": "2026-05-07T12:00:00.000Z",
      "status": 1,
      "timeZone": "string",
      "totalHours": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `allDay` | boolean |  |
| `approvalComment` | string |  |
| `approverPay` | number |  |
| `approverTime` | number |  |
| `comment` | string |  |
| `company` | number |  |
| `created` | date |  |
| `creator` | number |  |
| `dateEnd` | date |  |
| `dateEndAllDay` | boolean |  |
| `dateStart` | date |  |
| `dateStartAllDay` | boolean |  |
| `days` | number |  |
| `DPMetaData` | object |  |
| `employee` | number |  |
| `employeeHistory` | number |  |
| `employeeName` | string |  |
| `end` | number |  |
| `endTimeLocalized` | date |  |
| `externalId` | number |  |
| `id` | number |  |
| `leavePayLineArray` | array |  |
| `leaveRule` | number |  |
| `modified` | date |  |
| `notifyManagerArray` | array |  |
| `start` | number |  |
| `startTimeLocalized` | date |  |
| `status` | number |  |
| `timeZone` | string |  |
| `totalHours` | number |  |

## Native endpoint

Through the native Deputy API, this operation is `POST /api/v1/resource/Leave` (base URL `https://{{credentials.endpoint}}.deputy.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-leave-request.md) for the provider-specific parameters and requirements.

