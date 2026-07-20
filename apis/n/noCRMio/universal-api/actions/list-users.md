# noCRM.io: List Users

Retrieves users from noCRM.io.

```
GET https://connect.mindcloud.co/v1/universal/noCRMio/latest/actions/list-users
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a noCRM.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/noCRMio/latest/actions/list-users?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/noCRMio/latest/actions/list-users?${params}`, {
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
| `email` | string | no | Filter users by email. |
| `lastName` | string | no | Filter users by last name. |
| `firstName` | string | no | Filter users by first name. |
| `status` | string | no | User status filter. Default: `all`. |
| `direction` | string | no | Sort direction for returned users. Default: `asc`. |
| `role` | string | no | User role filter. Default: `all`. |
| `teams` | list<string> | no | Array of team IDs or names. Accepts multiple values in one string, delimited by `,`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "avatarUrl": {},
      "createdAt": "string",
      "email": "ava@example.com",
      "firstname": "Ava",
      "hasActivated": true,
      "id": 1,
      "im": {},
      "imType": {},
      "isAdmin": true,
      "isDisabled": true,
      "jobTitle": {},
      "lastname": "Chen",
      "locale": "string",
      "mobilePhone": {},
      "permalink": "https://example.com",
      "phone": {},
      "teams": [
        [
          "string"
        ]
      ],
      "timeZone": "string",
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `avatarUrl` | object |  |
| `createdAt` | string |  |
| `email` | string |  |
| `firstname` | string |  |
| `hasActivated` | boolean |  |
| `id` | number |  |
| `im` | object |  |
| `imType` | object |  |
| `isAdmin` | boolean |  |
| `isDisabled` | boolean |  |
| `jobTitle` | object |  |
| `lastname` | string |  |
| `locale` | string |  |
| `mobilePhone` | object |  |
| `permalink` | string |  |
| `phone` | object |  |
| `teams[]` | array<string> |  |
| `timeZone` | string |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native noCRM.io API, this operation is `GET /users` (base URL `{{credentials.baseUrl}}/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-users.md) for the provider-specific parameters and requirements.

