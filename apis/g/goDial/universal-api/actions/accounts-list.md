# GoDial: List Users

Retrieves a list of users from GoDial.

```
GET https://connect.mindcloud.co/v1/universal/goDial/latest/actions/accounts-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GoDial `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/goDial/latest/actions/accounts-list?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/goDial/latest/actions/accounts-list?${params}`, {
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
      "companyId": "string",
      "createdOn": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "forcePasswordReset": true,
      "id": "string",
      "isEmailVerified": true,
      "name": "Ava Chen",
      "permissions": {},
      "phone": "string",
      "role": "string",
      "teamsId": [
        "string"
      ],
      "username": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `companyId` | string | Owning company identifier. |
| `createdOn` | date | Account creation timestamp. |
| `email` | string | Account email address. |
| `forcePasswordReset` | boolean | Whether a password reset is required. |
| `id` | string | Account identifier. |
| `isEmailVerified` | boolean | Whether the email is verified. |
| `name` | string | Account name. |
| `permissions` | object | Permission flags for the account. |
| `phone` | string | Phone number. |
| `role` | string | Account role. |
| `teamsId` | array<string> | Associated team identifiers. |
| `username` | string | GoDial username. |

## Native endpoint

Through the native GoDial API, this operation is `GET /externals/accounts/list` (base URL `https://enterprise.godial.cc/meta/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/accounts-list.md) for the provider-specific parameters and requirements.

