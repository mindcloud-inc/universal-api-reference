# Kylas CRM: Get User

Retrieves a user from Kylas CRM by ID.

```
GET https://connect.mindcloud.co/v1/universal/kylasCRM/latest/actions/get-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kylas CRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kylasCRM/latest/actions/get-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kylasCRM/latest/actions/get-user?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `userId` | string | no | The Kylas user ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "confirmationTokenSentAt": "string",
      "confirmedAt": "string",
      "createdAt": "string",
      "createdBy": 1,
      "currency": "string",
      "customFieldValues": {},
      "dateFormat": "string",
      "deactivatedReason": "string",
      "department": "string",
      "designation": "string",
      "email": "ava@example.com",
      "emailVerified": true,
      "failedAttempts": 1,
      "firstName": "Ava",
      "id": 1,
      "language": "string",
      "lastName": "Chen",
      "locked": true,
      "lockedAt": "string",
      "metaData": {},
      "name": "Ava Chen",
      "ownerId": 1,
      "permissions": [
        "string"
      ],
      "phoneNumbers": [
        "string"
      ],
      "profileId": 1,
      "recordActions": {},
      "resetPasswordTokenSentAt": "string",
      "salutation": "string",
      "signature": "string",
      "timezone": "string",
      "title": "string",
      "unlockTokenSentAt": "string",
      "updatedAt": "string",
      "updatedBy": 1,
      "updatedEmail": "ava@example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean | Whether the user is active. |
| `confirmationTokenSentAt` | string | Timestamp when the confirmation token was sent. |
| `confirmedAt` | string | Timestamp when the user was confirmed. |
| `createdAt` | string | UTC timestamp when the user was created. |
| `createdBy` | number | User ID that created the user. |
| `currency` | string | Preferred currency code. |
| `customFieldValues` | object | Custom field values for the user. |
| `dateFormat` | string | Preferred date format. |
| `deactivatedReason` | string | Reason the user was deactivated. |
| `department` | string | Department name. |
| `designation` | string | User designation. |
| `email` | string | Primary email address. |
| `emailVerified` | boolean | Whether the user's email is verified. |
| `failedAttempts` | number | Failed login attempt count. |
| `firstName` | string | User first name. |
| `id` | number | Kylas user ID. |
| `language` | string | Configured language code. |
| `lastName` | string | User last name. |
| `locked` | boolean | Whether the user is locked. |
| `lockedAt` | string | Timestamp when the user was locked. |
| `metaData` | object | Additional Kylas metadata for related display names. |
| `name` | string | Full display name. |
| `ownerId` | number | Owner user ID for the user. |
| `permissions` | array | Permissions assigned to the user. |
| `phoneNumbers` | array | Phone numbers associated with the user. |
| `profileId` | number | Kylas profile ID. |
| `recordActions` | object | Action permissions available on this user record. |
| `resetPasswordTokenSentAt` | string | Timestamp when the reset password token was sent. |
| `salutation` | string | User salutation. |
| `signature` | string | Email signature or profile signature text. |
| `timezone` | string | Configured timezone. |
| `title` | string | User title. |
| `unlockTokenSentAt` | string | Timestamp when the unlock token was sent. |
| `updatedAt` | string | UTC timestamp when the user was last updated. |
| `updatedBy` | number | User ID that last updated the user. |
| `updatedEmail` | string | Pending updated email, if present. |

## Native endpoint

Through the native Kylas CRM API, this operation is `GET /users/{userId}` (base URL `https://api.kylas.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-user.md) for the provider-specific parameters and requirements.

