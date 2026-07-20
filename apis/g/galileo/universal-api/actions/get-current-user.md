# Galileo: Get Current User

Retrieves the current user from Galileo.

```
GET https://connect.mindcloud.co/v1/universal/galileo/latest/actions/get-current-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Galileo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/galileo/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/galileo/latest/actions/get-current-user?${params}`, {
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
      "authMethod": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "emailIsVerified": true,
      "firstName": "Ava",
      "genericPermissions": [
        {
          "action": "string",
          "allowed": true,
          "message": "string",
          "resource": "string"
        }
      ],
      "id": "string",
      "lastName": "Chen",
      "organizationId": "string",
      "organizationName": "Ava Chen",
      "permissions": [
        {
          "action": "string",
          "allowed": true,
          "message": "string"
        }
      ],
      "role": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `authMethod` | string |  |
| `createdAt` | date |  |
| `email` | string |  |
| `emailIsVerified` | boolean |  |
| `firstName` | string |  |
| `genericPermissions` | array<object> |  |
| `genericPermissions[].action` | string |  |
| `genericPermissions[].allowed` | boolean |  |
| `genericPermissions[].message` | string |  |
| `genericPermissions[].resource` | string |  |
| `id` | string |  |
| `lastName` | string |  |
| `organizationId` | string |  |
| `organizationName` | string |  |
| `permissions` | array<object> |  |
| `permissions[].action` | string |  |
| `permissions[].allowed` | boolean |  |
| `permissions[].message` | string |  |
| `role` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Galileo API, this operation is `GET /v2/current_user` (base URL `https://api.galileo.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-current-user.md) for the provider-specific parameters and requirements.

