# 7shifts: Create Time Punch

Creates a new time punch in 7shifts.

```
POST https://connect.mindcloud.co/v1/universal/shifts/latest/actions/create-time-punch
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a 7shifts `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/shifts/latest/actions/create-time-punch" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/shifts/latest/actions/create-time-punch', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "clocked_in": "2026-05-07T12:00:00.000Z",
      "clocked_out": "2026-05-07T12:00:00.000Z",
      "department_id": 1,
      "id": 1,
      "location_id": 1,
      "role_id": 1,
      "user_id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `clocked_in` | date |  |
| `clocked_out` | date |  |
| `department_id` | number |  |
| `id` | number |  |
| `location_id` | number |  |
| `role_id` | number |  |
| `user_id` | number |  |

## Native endpoint

Through the native 7shifts API, this operation is `POST /v2/company/{company_id}/time_punches` (base URL `https://api.7shifts.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-time-punch.md) for the provider-specific parameters and requirements.

