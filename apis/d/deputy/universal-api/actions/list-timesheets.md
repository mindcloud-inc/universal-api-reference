# Deputy: List Timesheets

Retrieves the timesheet list from Deputy.

```
GET https://connect.mindcloud.co/v1/universal/deputy/latest/actions/list-timesheets
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Deputy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/deputy/latest/actions/list-timesheets?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/deputy/latest/actions/list-timesheets?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "_DPMetaData": {},
      "Created": "2026-05-07T12:00:00.000Z",
      "Date": "2026-05-07T12:00:00.000Z",
      "Employee": 1,
      "EmployeeComment": "string",
      "EndTime": 1,
      "Id": 1,
      "IsLeave": true,
      "Modified": "2026-05-07T12:00:00.000Z",
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
| `Created` | date |  |
| `Date` | date |  |
| `Employee` | number |  |
| `EmployeeComment` | string |  |
| `EndTime` | number |  |
| `Id` | number |  |
| `IsLeave` | boolean |  |
| `Modified` | date |  |
| `Slots` | array<object> |  |
| `StartTime` | number |  |
| `TimeApproved` | boolean |  |
| `TotalTime` | number |  |

## Native endpoint

Through the native Deputy API, this operation is `POST /api/v1/resource/Timesheet/QUERY` (base URL `https://{{credentials.endpoint}}.deputy.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-timesheets.md) for the provider-specific parameters and requirements.

