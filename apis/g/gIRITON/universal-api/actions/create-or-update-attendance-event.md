# GIRITON: Create Or Update Attendance Event

Creates or updates an attendance event in GIRITON.

```
PUT https://connect.mindcloud.co/v1/universal/gIRITON/latest/actions/create-or-update-attendance-event
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GIRITON `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/gIRITON/latest/actions/create-or-update-attendance-event" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "startOrStop": true
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/gIRITON/latest/actions/create-or-update-attendance-event', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "startOrStop": true
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `userId` | string | no | User ID for the attendance event. |
| `attendanceActivityId` | string | no | Attendance activity ID for the event. |
| `dateTime` | string | no | Date time of the attendance event, for example 2026-04-30T09:00+02:00. |
| `startOrStop` | boolean | yes | Whether the attendance activity starts or stops at the given date time. |
| `note` | string | no | Optional attendance event note. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "count": 1,
      "entries": [
        {}
      ],
      "newestTimestamp": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `count` | number | Number of returned presence entries. |
| `entries` | array<object> | Presence entry records. |
| `newestTimestamp` | date | Newest entry timestamp. |

## Native endpoint

Through the native GIRITON API, this operation is `POST /attendance/attendanceEvent` (base URL `https://rest.giriton.com/system/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-or-update-attendance-event.md) for the provider-specific parameters and requirements.

