# 7shifts: List Time Punches

Lists the time punches in 7shifts.

```
GET https://connect.mindcloud.co/v1/universal/shifts/latest/actions/list-time-punches
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a 7shifts `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/shifts/latest/actions/list-time-punches?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/shifts/latest/actions/list-time-punches?${params}`, {
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

Through the native 7shifts API, this operation is `GET /v2/company/{company_id}/time_punches` (base URL `https://api.7shifts.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-time-punches.md) for the provider-specific parameters and requirements.

