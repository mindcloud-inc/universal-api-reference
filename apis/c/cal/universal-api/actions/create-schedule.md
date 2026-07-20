# Cal.com: Create Schedule

Creates a schedule in Cal.com.

```
POST https://connect.mindcloud.co/v1/universal/cal/latest/actions/create-schedule
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cal.com `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/cal/latest/actions/create-schedule" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "timeZone": "string",
  "isDefault": true
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cal/latest/actions/create-schedule', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "timeZone": "string",
    "isDefault": true
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Schedule name. |
| `timeZone` | string | yes | IANA time zone for the schedule. |
| `isDefault` | boolean | yes | Set true to make this the default schedule. |
| `availability[]` | array<object> | no | Availability windows for recurring weekly schedule blocks. |
| `availability[].days[]` | array<string> | no | Weekday list for an availability window. |
| `availability[].startTime` | string | no | Start time for an availability window. |
| `availability[].endTime` | string | no | End time for an availability window. |
| `overrides[]` | array<object> | no | Date-specific availability overrides. |
| `overrides[].date` | string | no | Override date in ISO date format. |
| `overrides[].startTime` | string | no | Start time for an override window. |
| `overrides[].endTime` | string | no | End time for an override window. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "availability": [
        {}
      ],
      "id": 1,
      "isDefault": true,
      "name": "Ava Chen",
      "overrides": [
        {}
      ],
      "ownerId": 1,
      "timeZone": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `availability` | array<object> |  |
| `id` | number |  |
| `isDefault` | boolean |  |
| `name` | string |  |
| `overrides` | array<object> |  |
| `ownerId` | number |  |
| `timeZone` | string |  |

## Native endpoint

Through the native Cal.com API, this operation is `POST /schedules` (base URL `https://api.cal.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-schedule.md) for the provider-specific parameters and requirements.

