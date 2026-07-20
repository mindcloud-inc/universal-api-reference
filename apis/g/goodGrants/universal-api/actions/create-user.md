# Good Grants: Create user

Creates a new user in Good Grants.

```
POST https://connect.mindcloud.co/v1/universal/goodGrants/latest/actions/create-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Good Grants `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/goodGrants/latest/actions/create-user" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "firstName": "Ava",
  "lastName": "Chen",
  "password": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/goodGrants/latest/actions/create-user', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "firstName": "Ava",
    "lastName": "Chen",
    "password": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `firstName` | string | yes | User first name |
| `lastName` | string | yes | User last name |
| `password` | string | yes | User password |
| `email` | string | no | User email |
| `mobile` | string | no | User mobile number |
| `roles[]` | array<string> | no | Role slugs |
| `preferences` | object | no | Notification preferences |
| `userFields` | object | no | Field slug to value map |

## Response

```json
{
  "success": true,
  "data": [
    {
      "analytics_cookies": true,
      "broadcast_emails": true,
      "comments": "string",
      "confirmation": "string",
      "confirmed_at": "2026-05-07T12:00:00.000Z",
      "created_at": "2026-05-07T12:00:00.000Z",
      "created_by": "string",
      "email": "ava@example.com",
      "first_name": "Ava",
      "language": {},
      "last_name": "Chen",
      "marketing_cookies": true,
      "mobile": "string",
      "name": "Ava Chen",
      "necessary_cookies": true,
      "notification_emails": true,
      "notification_sms": true,
      "preferences": {},
      "roles": [
        {}
      ],
      "slug": "string",
      "social_sharing": true,
      "updated": "2026-05-07T12:00:00.000Z",
      "user_fields": [
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
| `analytics_cookies` | boolean |  |
| `broadcast_emails` | boolean |  |
| `comments` | string |  |
| `confirmation` | string |  |
| `confirmed_at` | date |  |
| `created_at` | date |  |
| `created_by` | string |  |
| `email` | string |  |
| `first_name` | string |  |
| `language` | object |  |
| `last_name` | string |  |
| `marketing_cookies` | boolean |  |
| `mobile` | string |  |
| `name` | string |  |
| `necessary_cookies` | boolean |  |
| `notification_emails` | boolean |  |
| `notification_sms` | boolean |  |
| `preferences` | object |  |
| `roles` | array<object> |  |
| `slug` | string |  |
| `social_sharing` | boolean |  |
| `updated` | date |  |
| `user_fields` | array<object> |  |

## Native endpoint

Through the native Good Grants API, this operation is `POST user` (base URL `https://api.cr4ce.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-user.md) for the provider-specific parameters and requirements.

