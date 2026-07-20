# 7shifts: Deactivate User

Deactivates an existing user in 7shifts.

```
DELETE https://connect.mindcloud.co/v1/universal/shifts/latest/actions/deactivate-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a 7shifts `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/shifts/latest/actions/deactivate-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/shifts/latest/actions/deactivate-user?${params}`, {
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
      "active": true,
      "first_name": "Ava",
      "id": 1,
      "last_name": "Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `first_name` | string |  |
| `id` | number |  |
| `last_name` | string |  |

## Native endpoint

Through the native 7shifts API, this operation is `DELETE /v2/company/{company_id}/users/{identifier}` (base URL `https://api.7shifts.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/deactivate-user.md) for the provider-specific parameters and requirements.

