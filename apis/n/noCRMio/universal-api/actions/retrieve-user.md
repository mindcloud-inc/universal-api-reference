# noCRM.io: Retrieve User

Retrieves user details from noCRM.io.

```
GET https://connect.mindcloud.co/v1/universal/noCRMio/latest/actions/retrieve-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a noCRM.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/noCRMio/latest/actions/retrieve-user?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/noCRMio/latest/actions/retrieve-user?${params}`, {
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
| `id` | string | yes | User ID or email address. |

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

Through the native noCRM.io API, this operation is `GET /users/:id` (base URL `{{credentials.baseUrl}}/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-user.md) for the provider-specific parameters and requirements.

