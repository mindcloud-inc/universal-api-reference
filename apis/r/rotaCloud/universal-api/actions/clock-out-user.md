# RotaCloud: Clock Out User



```
PUT https://connect.mindcloud.co/v1/universal/rotaCloud/latest/actions/clock-out-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RotaCloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/rotaCloud/latest/actions/clock-out-user" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "action": "string",
  "id": 1,
  "method": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rotaCloud/latest/actions/clock-out-user', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "action": "string",
    "id": 1,
    "method": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `action` | string | yes | Clock-out action value. |
| `id` | number | yes | User ID to clock out. |
| `method` | string | yes | Clock-out method. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "approved": true,
      "deleted": true,
      "hours": 1,
      "hours_auto": 1,
      "hours_is_auto": true,
      "id": 1,
      "in_device": "string",
      "in_location": {},
      "in_method": "string",
      "in_terminal": 1,
      "in_time": 1,
      "location": 1,
      "minutes_break": 1,
      "minutes_late": 1,
      "notes": "string",
      "out_device": "string",
      "out_location": {},
      "out_method": "string",
      "out_terminal": 1,
      "out_time": 1,
      "role": 1,
      "shift": {},
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
| `hours_auto` | number |  |
| `hours_is_auto` | boolean |  |
| `id` | number |  |
| `in_device` | string |  |
| `in_location` | object |  |
| `in_method` | string |  |
| `in_terminal` | number |  |
| `in_time` | number |  |
| `location` | number |  |
| `minutes_break` | number |  |
| `minutes_late` | number |  |
| `notes` | string |  |
| `out_device` | string |  |
| `out_location` | object |  |
| `out_method` | string |  |
| `out_terminal` | number |  |
| `out_time` | number |  |
| `role` | number |  |
| `shift` | object |  |
| `user` | number |  |

## Native endpoint

Through the native RotaCloud API, this operation is `POST /v1/users_clocked_in/:id` (base URL `https://api.rotacloud.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/clock-out-user.md) for the provider-specific parameters and requirements.

