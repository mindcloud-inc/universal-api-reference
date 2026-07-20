# Appwrite: Create user with Scrypt modified password

Creates a new user with Scrypt modified password in your Appwrite project.

```
POST https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/users-create-scrypt-modified-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Appwrite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/users-create-scrypt-modified-user" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "userId": "string",
  "email": "ava@example.com",
  "password": "string",
  "passwordSalt": "string",
  "passwordSaltSeparator": "string",
  "passwordSignerKey": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/users-create-scrypt-modified-user', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "userId": "string",
    "email": "ava@example.com",
    "password": "string",
    "passwordSalt": "string",
    "passwordSaltSeparator": "string",
    "passwordSignerKey": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `userId` | string | yes | User ID. Choose a custom ID or generate a random ID with `ID.unique()`. Valid chars are a-z, A-Z, 0-9, period, hyphen, and underscore. Can't start with a special char. Max length is 36 chars. |
| `email` | string | yes | User email. |
| `password` | string | yes | User password hashed using Scrypt Modified. |
| `passwordSalt` | string | yes | Salt used to hash password. |
| `passwordSaltSeparator` | string | yes | Salt separator used to hash password. |
| `passwordSignerKey` | string | yes | Signer key used to hash password. |
| `name` | string | no | User name. Max length: 128 chars. |

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

Through the native Appwrite API, this operation is `POST /users/scrypt-modified` (base URL `https://cloud.appwrite.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/users-create-scrypt-modified-user.md) for the provider-specific parameters and requirements.

