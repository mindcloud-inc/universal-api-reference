# Deputy: Get Timesheet Details

Retrieves detailed timesheet data from Deputy.

```
GET https://connect.mindcloud.co/v1/universal/deputy/latest/actions/get-timesheet-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Deputy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/deputy/latest/actions/get-timesheet-details?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/deputy/latest/actions/get-timesheet-details?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes | Timesheet ID from Deputy. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_DPMetaData": {},
      "CompanyObject": {},
      "Created": "2026-05-07T12:00:00.000Z",
      "Date": "2026-05-07T12:00:00.000Z",
      "Employee": 1,
      "EmployeeComment": "string",
      "EmployeeObject": {},
      "EndTime": 1,
      "Id": 1,
      "IsLeave": true,
      "Modified": "2026-05-07T12:00:00.000Z",
      "OperationalUnitObject": {},
      "Slots": [
        {}
      ],
      "StartTime": 1,
      "TimeApproved": true,
      "TotalTime": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_DPMetaData` | object |  |
| `CompanyObject` | object |  |
| `Created` | date |  |
| `Date` | date |  |
| `Employee` | number |  |
| `EmployeeComment` | string |  |
| `EmployeeObject` | object |  |
| `EndTime` | number |  |
| `Id` | number |  |
| `IsLeave` | boolean |  |
| `Modified` | date |  |
| `OperationalUnitObject` | object |  |
| `Slots` | array<object> |  |
| `StartTime` | number |  |
| `TimeApproved` | boolean |  |
| `TotalTime` | number |  |

## Native endpoint

Through the native Deputy API, this operation is `GET /api/v1/supervise/timesheet/:id/details` (base URL `https://{{credentials.endpoint}}.deputy.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-timesheet-details.md) for the provider-specific parameters and requirements.

