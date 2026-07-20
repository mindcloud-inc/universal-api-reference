# 7shifts: List Users Authorized Locations

Lists a user's authorized locations in 7shifts.

```
GET https://connect.mindcloud.co/v1/universal/shifts/latest/actions/list-users-authorized-locations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a 7shifts `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/shifts/latest/actions/list-users-authorized-locations?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/shifts/latest/actions/list-users-authorized-locations?${params}`, {
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

Through the native 7shifts API, this operation is `GET /v2/company/{company_id}/users/{user_id}/authorized_locations` (base URL `https://api.7shifts.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-users-authorized-locations.md) for the provider-specific parameters and requirements.

