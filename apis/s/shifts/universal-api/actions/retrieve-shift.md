# 7shifts: Retrieve Shift

Retrieves current shift details from 7shifts.

```
GET https://connect.mindcloud.co/v1/universal/shifts/latest/actions/retrieve-shift
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a 7shifts `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/shifts/latest/actions/retrieve-shift?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/shifts/latest/actions/retrieve-shift?${params}`, {
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
      "department_id": 1,
      "end": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "location_id": 1,
      "role_id": 1,
      "start": "2026-05-07T12:00:00.000Z",
      "user_id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `department_id` | number |  |
| `end` | date |  |
| `id` | number |  |
| `location_id` | number |  |
| `role_id` | number |  |
| `start` | date |  |
| `user_id` | number |  |

## Native endpoint

Through the native 7shifts API, this operation is `GET /v2/company/{company_id}/shifts/{shift_id}` (base URL `https://api.7shifts.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-shift.md) for the provider-specific parameters and requirements.

