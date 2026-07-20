# Appwrite: Update status

Updates the status in your Appwrite project.

```
PUT https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/account-update-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Appwrite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/account-update-status" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/account-update-status', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "$createdAt": "string",
      "$id": "string",
      "$updatedAt": "string",
      "accessedAt": "string",
      "email": "ava@example.com",
      "emailVerification": true,
      "hash": "string",
      "hashOptions": {},
      "labels": [
        "string"
      ],
      "mfa": true,
      "name": "Ava Chen",
      "password": "string",
      "passwordUpdate": "string",
      "phone": "string",
      "phoneVerification": true,
      "prefs": {},
      "registration": "string",
      "status": true,
      "targets": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `$createdAt` | string | User creation date in ISO 8601 format. |
| `$id` | string | User ID. |
| `$updatedAt` | string | User update date in ISO 8601 format. |
| `accessedAt` | string | Most recent access date in ISO 8601 format. This attribute is only updated again after 24 hours. |
| `email` | string | User email address. |
| `emailVerification` | boolean | Email verification status. |
| `hash` | string | Password hashing algorithm. |
| `hashOptions` | object | Password hashing algorithm configuration. |
| `labels` | array<string> | Labels for the user. |
| `mfa` | boolean | Multi factor authentication status. |
| `name` | string | User name. |
| `password` | string | Hashed user password. |
| `passwordUpdate` | string | Password update time in ISO 8601 format. |
| `phone` | string | User phone number in E.164 format. |
| `phoneVerification` | boolean | Phone verification status. |
| `prefs` | object | User preferences as a key-value object |
| `registration` | string | User registration date in ISO 8601 format. |
| `status` | boolean | User status. Pass `true` for enabled and `false` for disabled. |
| `targets` | array<object> | A user-owned message receiver. A single user may have multiple e.g. emails, phones, and a browser. Each target is registered with a single provider. |

## Native endpoint

Through the native Appwrite API, this operation is `PATCH /account/status` (base URL `https://cloud.appwrite.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/account-update-status.md) for the provider-specific parameters and requirements.

