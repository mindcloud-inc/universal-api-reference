# 7shifts: Update Department

Updates an existing department in 7shifts.

```
PUT https://connect.mindcloud.co/v1/universal/shifts/latest/actions/update-department
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a 7shifts `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/shifts/latest/actions/update-department" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/shifts/latest/actions/update-department', {
  method: 'PUT',
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
      "id": 1,
      "location_id": 1,
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number |  |
| `location_id` | number |  |
| `name` | string |  |

## Native endpoint

Through the native 7shifts API, this operation is `PUT /v2/company/{company_id}/departments/{department_id}` (base URL `https://api.7shifts.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-department.md) for the provider-specific parameters and requirements.

