# SimpliRoute: List Users

Retrieves drivers from SimpliRoute.

```
GET https://connect.mindcloud.co/v1/universal/simpliRoute/latest/actions/list-users
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SimpliRoute `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/simpliRoute/latest/actions/list-users?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/simpliRoute/latest/actions/list-users?${params}`, {
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
      "created": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "expired_documents": [
        {}
      ],
      "id": 1,
      "is_admin": true,
      "is_driver": true,
      "is_staff": true,
      "last_login": "2026-05-07T12:00:00.000Z",
      "modified": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "old_id": 1,
      "phone": "string",
      "status": "string",
      "username": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created` | date |  |
| `email` | string |  |
| `expired_documents` | array<object> |  |
| `id` | number |  |
| `is_admin` | boolean |  |
| `is_driver` | boolean |  |
| `is_staff` | boolean |  |
| `last_login` | date |  |
| `modified` | date |  |
| `name` | string |  |
| `old_id` | number |  |
| `phone` | string |  |
| `status` | string |  |
| `username` | string |  |

## Native endpoint

Through the native SimpliRoute API, this operation is `GET /v1/accounts/drivers/` (base URL `https://api.simpliroute.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-users.md) for the provider-specific parameters and requirements.

