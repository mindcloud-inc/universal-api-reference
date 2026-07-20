# Yousign: List Users

Retrieves users from Yousign.

```
GET https://connect.mindcloud.co/v1/universal/yousign/latest/actions/list-users
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Yousign `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/yousign/latest/actions/list-users?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/yousign/latest/actions/list-users?${params}`, {
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
| `after` | string | no | Return users after this pagination cursor. |
| `limit` | number | no | Maximum number of users to return. |
| `email` | string | no | Filter users by email address. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "avatar": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "firstName": "Ava",
      "id": "string",
      "isActive": true,
      "jobTitle": "string",
      "lastName": "Chen",
      "locale": "string",
      "phoneNumber": "string",
      "role": "string",
      "source": "string",
      "status": "string",
      "workspaces": [
        {
          "id": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `avatar` | string | User avatar URL. |
| `createdAt` | date | User creation timestamp. |
| `email` | string | User email address. |
| `firstName` | string | User first name. |
| `id` | string | User ID. |
| `isActive` | boolean | Whether the user is active. |
| `jobTitle` | string | User job title. |
| `lastName` | string | User last name. |
| `locale` | string | User locale. |
| `phoneNumber` | string | User phone number in E.164 format. |
| `role` | string | User role. |
| `source` | string | Source that created the user. |
| `status` | string | User lifecycle status. |
| `workspaces[].id` | string | Workspace ID visible to the user. |

## Native endpoint

Through the native Yousign API, this operation is `GET /users` (base URL `https://api-sandbox.yousign.app/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-users.md) for the provider-specific parameters and requirements.

