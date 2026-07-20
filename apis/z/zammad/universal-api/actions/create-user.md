# Zammad: Create User

Creates a new user in Zammad.

```
POST https://connect.mindcloud.co/v1/universal/zammad/latest/actions/create-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zammad `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/zammad/latest/actions/create-user" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "firstname": "MC TEST",
  "lastname": "20260413 1700",
  "email": "mc.test@example.com",
  "login": "mc.test@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zammad/latest/actions/create-user', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "firstname": "MC TEST",
    "lastname": "20260413 1700",
    "email": "mc.test@example.com",
    "login": "mc.test@example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `firstname` | string | yes | User first name. Example: `MC TEST`. |
| `lastname` | string | yes | User last name. Example: `20260413 1700`. |
| `email` | string | yes | User email address. Example: `mc.test@example.com`. |
| `login` | string | yes | Unique login for the user. Example: `mc.test@example.com`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "address": {},
      "city": "string",
      "country": "string",
      "createdAt": "string",
      "createdById": 1,
      "department": {},
      "email": "ava@example.com",
      "fax": "string",
      "firstname": "Ava",
      "id": 1,
      "image": {},
      "imageSource": {},
      "lastLogin": {},
      "lastname": "Chen",
      "login": "string",
      "loginFailed": 1,
      "mobile": "string",
      "note": "string",
      "organizationId": {},
      "outOfOffice": true,
      "outOfOfficeEndAt": {},
      "outOfOfficeReplacementId": {},
      "outOfOfficeStartAt": {},
      "phone": "string",
      "preferences": {
        "locale": "string"
      },
      "roleIds": [
        1
      ],
      "source": {},
      "street": "string",
      "updatedAt": "string",
      "updatedById": 1,
      "verified": true,
      "vip": true,
      "web": "string",
      "zip": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `address` | object |  |
| `city` | string |  |
| `country` | string |  |
| `createdAt` | string |  |
| `createdById` | number |  |
| `department` | object |  |
| `email` | string |  |
| `fax` | string |  |
| `firstname` | string |  |
| `id` | number |  |
| `image` | object |  |
| `imageSource` | object |  |
| `lastLogin` | object |  |
| `lastname` | string |  |
| `login` | string |  |
| `loginFailed` | number |  |
| `mobile` | string |  |
| `note` | string |  |
| `organizationId` | object |  |
| `outOfOffice` | boolean |  |
| `outOfOfficeEndAt` | object |  |
| `outOfOfficeReplacementId` | object |  |
| `outOfOfficeStartAt` | object |  |
| `phone` | string |  |
| `preferences.locale` | string |  |
| `roleIds[]` | number |  |
| `source` | object |  |
| `street` | string |  |
| `updatedAt` | string |  |
| `updatedById` | number |  |
| `verified` | boolean |  |
| `vip` | boolean |  |
| `web` | string |  |
| `zip` | string |  |

## Native endpoint

Through the native Zammad API, this operation is `POST /users` (base URL `{{credentials.baseUrl}}/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-user.md) for the provider-specific parameters and requirements.

