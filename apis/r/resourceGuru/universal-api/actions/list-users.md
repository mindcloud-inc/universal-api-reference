# Resource Guru: List Users

Retrieves users from Resource Guru.

```
GET https://connect.mindcloud.co/v1/universal/resourceGuru/latest/actions/list-users
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Resource Guru `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/resourceGuru/latest/actions/list-users?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/resourceGuru/latest/actions/list-users?${params}`, {
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
      "activation_state": "string",
      "booking_rights": "string",
      "client_rights": "string",
      "created_at": "string",
      "downtime_rights": "string",
      "email": "ava@example.com",
      "first_name": "Ava",
      "id": 1,
      "image": "string",
      "images": {},
      "last_activity_at": "string",
      "last_login_at": "string",
      "last_logout_at": "string",
      "last_name": "Chen",
      "last_product_update_read_at": "string",
      "owner": true,
      "permissions": "string",
      "project_rights": "string",
      "report_rights": "string",
      "resource_rights": "string",
      "timesheet_rights": "string",
      "timezone": "string",
      "updated_at": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `activation_state` | string |  |
| `booking_rights` | string |  |
| `client_rights` | string |  |
| `created_at` | string |  |
| `downtime_rights` | string |  |
| `email` | string |  |
| `first_name` | string |  |
| `id` | number |  |
| `image` | string |  |
| `images` | object |  |
| `last_activity_at` | string |  |
| `last_login_at` | string |  |
| `last_logout_at` | string |  |
| `last_name` | string |  |
| `last_product_update_read_at` | string |  |
| `owner` | boolean |  |
| `permissions` | string |  |
| `project_rights` | string |  |
| `report_rights` | string |  |
| `resource_rights` | string |  |
| `timesheet_rights` | string |  |
| `timezone` | string |  |
| `updated_at` | string |  |

## Native endpoint

Through the native Resource Guru API, this operation is `GET /users` (base URL `https://api.resourceguruapp.com/v1/{{credentials.accountId}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-users.md) for the provider-specific parameters and requirements.

