# Umbrella: List Users

Retrieves user accounts from your Umbrella organization.

```
GET https://connect.mindcloud.co/v1/universal/umbrella/latest/actions/list-users
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Umbrella `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/umbrella/latest/actions/list-users?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/umbrella/latest/actions/list-users?${params}`, {
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
      "email": "ava@example.com",
      "firstname": "Ava",
      "id": 1,
      "lastLoginTime": "2026-05-07T12:00:00.000Z",
      "lastname": "Chen",
      "role": "string",
      "roleId": 1,
      "status": "string",
      "timezone": "string",
      "twoFactorEnable": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `email` | string |  |
| `firstname` | string |  |
| `id` | number |  |
| `lastLoginTime` | date |  |
| `lastname` | string |  |
| `role` | string |  |
| `roleId` | number |  |
| `status` | string |  |
| `timezone` | string |  |
| `twoFactorEnable` | boolean |  |

## Native endpoint

Through the native Umbrella API, this operation is `GET /admin/v2/users` (base URL `https://api.umbrella.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-users.md) for the provider-specific parameters and requirements.

