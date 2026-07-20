# Vtiger CRM: Get Current User

Retrieves the current user profile from Vtiger CRM.

```
GET https://connect.mindcloud.co/v1/universal/vtigerCRM/latest/actions/get-current-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vtiger CRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vtigerCRM/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vtigerCRM/latest/actions/get-current-user?${params}`, {
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
      "email1": "ava@example.com",
      "first_name": "Ava",
      "id": "string",
      "is_admin": "string",
      "last_name": "Chen",
      "user_name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `email1` | string | Primary email address. |
| `first_name` | string | User first name. |
| `id` | string | Vtiger user id. |
| `is_admin` | string | Whether the user is an administrator. |
| `last_name` | string | User last name. |
| `user_name` | string | Vtiger username. |

## Native endpoint

Through the native Vtiger CRM API, this operation is `GET /me` (base URL `{{credentials.apiBaseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-current-user.md) for the provider-specific parameters and requirements.

