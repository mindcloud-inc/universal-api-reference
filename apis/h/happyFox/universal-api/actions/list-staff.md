# HappyFox: List Staff

Retrieves staff members from HappyFox.

```
GET https://connect.mindcloud.co/v1/universal/happyFox/latest/actions/list-staff
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HappyFox `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/happyFox/latest/actions/list-staff?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/happyFox/latest/actions/list-staff?${params}`, {
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
      "categories": [
        1
      ],
      "email": "ava@example.com",
      "id": 1,
      "isAccountAdmin": true,
      "name": "Ava Chen",
      "permissions": [
        "string"
      ],
      "role": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean | Whether the staff member is active. |
| `categories` | array<number> | Category IDs assigned to the staff member. |
| `email` | string | Staff member email address. |
| `id` | number | HappyFox staff member ID. |
| `isAccountAdmin` | boolean | Whether the staff member is an account administrator. |
| `name` | string | Staff member display name. |
| `permissions` | array<string> | Granted permission slugs for the staff member. |
| `role` | object | Role assigned to the staff member. |

## Native endpoint

Through the native HappyFox API, this operation is `GET /staff/` (base URL `https://{{credentials.accountDomain}}/api/1.1/json`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-staff.md) for the provider-specific parameters and requirements.

