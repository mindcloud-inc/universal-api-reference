# GIRITON: List Attendance Activities

Retrieves available attendance activities from GIRITON.

```
GET https://connect.mindcloud.co/v1/universal/gIRITON/latest/actions/list-attendance-activities
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GIRITON `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gIRITON/latest/actions/list-attendance-activities?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gIRITON/latest/actions/list-attendance-activities?${params}`, {
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
      "canBePlanned": true,
      "canBeRequested": true,
      "color": "string",
      "counted": true,
      "dailyDataType": "string",
      "dataType": "string",
      "departments": [
        {}
      ],
      "description": "string",
      "displayStart": true,
      "displayStop": true,
      "entryTimestamp": "2026-05-07T12:00:00.000Z",
      "guid": "string",
      "id": "string",
      "mark": "string",
      "monthlyDataType": "string",
      "name": "Ava Chen",
      "number": "string",
      "renamedStart": "Ava Chen",
      "renamedStop": "Ava Chen",
      "selectStartTimes": [
        "string"
      ],
      "selectStopTimes": [
        "string"
      ],
      "shortcut": "string",
      "startColor": "string",
      "startIcon": "string",
      "stopColor": "string",
      "stopIcon": "string",
      "tags": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `canBePlanned` | boolean | Whether this activity can be planned. |
| `canBeRequested` | boolean | Whether users can request this activity. |
| `color` | string | Activity color. |
| `counted` | boolean | Whether the activity is counted. |
| `dailyDataType` | string | Daily data type. |
| `dataType` | string | Activity data type. |
| `departments` | array<object> | Associated departments. |
| `description` | string | Activity description. |
| `displayStart` | boolean | Whether start is displayed. |
| `displayStop` | boolean | Whether stop is displayed. |
| `entryTimestamp` | date | Activity entry timestamp. |
| `guid` | string | Activity GUID. |
| `id` | string | Attendance activity ID. |
| `mark` | string | Activity mark. |
| `monthlyDataType` | string | Monthly data type. |
| `name` | string | Activity name. |
| `number` | string | Activity number. |
| `renamedStart` | string | Custom start label. |
| `renamedStop` | string | Custom stop label. |
| `selectStartTimes` | array<string> | Selectable start times. |
| `selectStopTimes` | array<string> | Selectable stop times. |
| `shortcut` | string | Activity shortcut. |
| `startColor` | string | Start color. |
| `startIcon` | string | Start icon. |
| `stopColor` | string | Stop color. |
| `stopIcon` | string | Stop icon. |
| `tags` | array<string> | Activity tags. |

## Native endpoint

Through the native GIRITON API, this operation is `GET /attendance/attendanceActivities` (base URL `https://rest.giriton.com/system/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-attendance-activities.md) for the provider-specific parameters and requirements.

