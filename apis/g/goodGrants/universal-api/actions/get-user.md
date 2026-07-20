# Good Grants: Get user

Retrieves a user from Good Grants by slug or email.

```
GET https://connect.mindcloud.co/v1/universal/goodGrants/latest/actions/get-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Good Grants `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/goodGrants/latest/actions/get-user?connectionId=$CONNECTION_ID&identifier=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "identifier": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/goodGrants/latest/actions/get-user?${params}`, {
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
| `identifier` | string | yes | User slug or email. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "analyticsCookies": true,
      "broadcastEmails": true,
      "comments": "string",
      "confirmation": "string",
      "confirmedAt": "2026-05-07T12:00:00.000Z",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "createdBy": "string",
      "email": "ava@example.com",
      "firstName": "Ava",
      "language": {},
      "lastName": "Chen",
      "marketingCookies": true,
      "mobile": "string",
      "name": "Ava Chen",
      "necessaryCookies": true,
      "notificationEmails": true,
      "notificationSms": true,
      "preferences": {},
      "roles": [
        {}
      ],
      "slug": "string",
      "socialSharing": true,
      "updated": "2026-05-07T12:00:00.000Z",
      "userFields": [
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
| `analyticsCookies` | boolean |  |
| `broadcastEmails` | boolean |  |
| `comments` | string |  |
| `confirmation` | string |  |
| `confirmedAt` | date |  |
| `createdAt` | date |  |
| `createdBy` | string |  |
| `email` | string |  |
| `firstName` | string |  |
| `language` | object |  |
| `lastName` | string |  |
| `marketingCookies` | boolean |  |
| `mobile` | string |  |
| `name` | string |  |
| `necessaryCookies` | boolean |  |
| `notificationEmails` | boolean |  |
| `notificationSms` | boolean |  |
| `preferences` | object |  |
| `roles` | array<object> |  |
| `slug` | string |  |
| `socialSharing` | boolean |  |
| `updated` | date |  |
| `userFields` | array<object> |  |

## Native endpoint

Through the native Good Grants API, this operation is `GET user/:identifier` (base URL `https://api.cr4ce.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-user.md) for the provider-specific parameters and requirements.

