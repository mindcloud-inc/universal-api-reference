# QDS: Get Current User



```
GET https://connect.mindcloud.co/v1/universal/qDS/latest/actions/get-current-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a QDS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/qDS/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/qDS/latest/actions/get-current-user?${params}`, {
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
      "account": {
        "admin_email": "ava@example.com",
        "admin_name": "Ava Chen",
        "created_at": "2026-05-07T12:00:00.000Z",
        "finished_registration": 1,
        "id": 1,
        "locked_out": true,
        "name": "Ava Chen",
        "on_trial": true,
        "status": "string"
      },
      "restrictions": [
        "string"
      ],
      "user": {
        "email": "ava@example.com",
        "hr_user_settings": {
          "canSeeOwn": true,
          "canViewCompany": true,
          "canViewInternal": true,
          "role_id": 1
        },
        "id": 1,
        "is_super_admin": true,
        "name": "Ava Chen",
        "role_id": 1,
        "role": {
          "created_at": "2026-05-07T12:00:00.000Z",
          "description": "string",
          "id": 1,
          "key": "string",
          "name": "Ava Chen",
          "updated_at": "2026-05-07T12:00:00.000Z"
        }
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `account.admin_email` | string |  |
| `account.admin_name` | string |  |
| `account.created_at` | date |  |
| `account.finished_registration` | number |  |
| `account.id` | number |  |
| `account.locked_out` | boolean |  |
| `account.name` | string |  |
| `account.on_trial` | boolean |  |
| `account.status` | string |  |
| `restrictions[]` | string |  |
| `user.email` | string |  |
| `user.hr_user_settings.canSeeOwn` | boolean |  |
| `user.hr_user_settings.canViewCompany` | boolean |  |
| `user.hr_user_settings.canViewInternal` | boolean |  |
| `user.hr_user_settings.role_id` | number |  |
| `user.id` | number |  |
| `user.is_super_admin` | boolean |  |
| `user.name` | string |  |
| `user.role_id` | number |  |
| `user.role.created_at` | date |  |
| `user.role.description` | string |  |
| `user.role.id` | number |  |
| `user.role.key` | string |  |
| `user.role.name` | string |  |
| `user.role.updated_at` | date |  |

## Native endpoint

Through the native QDS API, this operation is `GET /user/current` (base URL `https://qdsapp.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-current-user.md) for the provider-specific parameters and requirements.

