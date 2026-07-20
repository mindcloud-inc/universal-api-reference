# GIRITON: Get Person Attendance Data

Retrieves configured attendance data for one GIRITON person.

```
GET https://connect.mindcloud.co/v1/universal/gIRITON/latest/actions/get-person-attendance-data
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GIRITON `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gIRITON/latest/actions/get-person-attendance-data?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gIRITON/latest/actions/get-person-attendance-data?${params}`, {
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
| `personId` | string | no | ID of the required person. |
| `personNumber` | string | no | Person number of the required person. |
| `dateFrom` | string | no | Beginning of the attendance time period. |
| `dateTo` | string | no | End of the attendance time period. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attendanceBlocks": [
        {}
      ],
      "attendanceEntries": [
        {}
      ],
      "businessTrips": [
        {}
      ],
      "dailyAttendanceGraphics": [
        {}
      ],
      "dailyAttendanceResults": [
        {}
      ],
      "dailyProjectGraphics": [
        {}
      ],
      "dailyProjectResults": [
        {}
      ],
      "monthlyAttendanceResults": [
        {}
      ],
      "monthlyProjectResults": [
        {}
      ],
      "person": {},
      "projectPlan": [
        {}
      ],
      "shiftPlan": [
        {}
      ],
      "vacations": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attendanceBlocks` | array<object> | Attendance block records. |
| `attendanceEntries` | array<object> | Attendance entry records. |
| `businessTrips` | array<object> | Business trip records. |
| `dailyAttendanceGraphics` | array<object> | Daily attendance graphic records. |
| `dailyAttendanceResults` | array<object> | Daily attendance result records. |
| `dailyProjectGraphics` | array<object> | Daily project graphic records. |
| `dailyProjectResults` | array<object> | Daily project result records. |
| `monthlyAttendanceResults` | array<object> | Monthly attendance result records. |
| `monthlyProjectResults` | array<object> | Monthly project result records. |
| `person` | object | Person details when attendance data is returned. |
| `projectPlan` | array<object> | Project calendar records. |
| `shiftPlan` | array<object> | Shift calendar records. |
| `vacations` | array<object> | Vacation records. |

## Native endpoint

Through the native GIRITON API, this operation is `GET /attendance/personAttendanceData` (base URL `https://rest.giriton.com/system/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-person-attendance-data.md) for the provider-specific parameters and requirements.

