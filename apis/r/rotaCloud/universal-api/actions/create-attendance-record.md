# RotaCloud: Create Attendance Record

Creates an attendance record in RotaCloud.

```
POST https://connect.mindcloud.co/v1/universal/rotaCloud/latest/actions/create-attendance-record
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RotaCloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/rotaCloud/latest/actions/create-attendance-record" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "in_time": 1,
  "user": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rotaCloud/latest/actions/create-attendance-record', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "in_time": 1,
    "user": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `in_time` | number | yes | Clock-in time as a Unix timestamp. |
| `user` | number | yes | ID of the user to clock in. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "approved": true,
      "deleted": true,
      "hours": 1,
      "id": 1,
      "in_time": 1,
      "location": 1,
      "minutes_break": 1,
      "out_time": 1,
      "role": 1,
      "user": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `approved` | boolean |  |
| `deleted` | boolean |  |
| `hours` | number |  |
| `id` | number |  |
| `in_time` | number |  |
| `location` | number |  |
| `minutes_break` | number |  |
| `out_time` | number |  |
| `role` | number |  |
| `user` | number |  |

## Native endpoint

Through the native RotaCloud API, this operation is `POST /v1/attendance` (base URL `https://api.rotacloud.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-attendance-record.md) for the provider-specific parameters and requirements.

