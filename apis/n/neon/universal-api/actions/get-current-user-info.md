# Neon: Retrieve current user details

Retrieves current user details from Neon.

```
GET https://connect.mindcloud.co/v1/universal/neon/latest/actions/get-current-user-info
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Neon `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/neon/latest/actions/get-current-user-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/neon/latest/actions/get-current-user-info?${params}`, {
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
      "active_seconds_limit": 1,
      "auth_accounts": [
        {}
      ],
      "billing_account": {},
      "branches_limit": 1,
      "compute_seconds_limit": 1,
      "email": "ava@example.com",
      "id": "string",
      "image": "string",
      "last_name": "Chen",
      "login": "string",
      "max_autoscaling_limit": 1,
      "name": "Ava Chen",
      "plan": "string",
      "projects_limit": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active_seconds_limit` | number |  |
| `auth_accounts` | array<object> |  |
| `billing_account` | object |  |
| `branches_limit` | number |  |
| `compute_seconds_limit` | number |  |
| `email` | string |  |
| `id` | string |  |
| `image` | string |  |
| `last_name` | string |  |
| `login` | string |  |
| `max_autoscaling_limit` | number |  |
| `name` | string |  |
| `plan` | string |  |
| `projects_limit` | number |  |

## Native endpoint

Through the native Neon API, this operation is `GET /users/me` (base URL `https://console.neon.tech/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-current-user-info.md) for the provider-specific parameters and requirements.

