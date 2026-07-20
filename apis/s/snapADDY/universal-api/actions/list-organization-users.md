# snapADDY: List Organization Users



```
GET https://connect.mindcloud.co/v1/universal/snapADDY/latest/actions/list-organization-users
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a snapADDY `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/snapADDY/latest/actions/list-organization-users?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/snapADDY/latest/actions/list-organization-users?${params}`, {
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
      "id": "string",
      "isAdmin": true,
      "isTerminalUser": true,
      "name": "Ava Chen",
      "organizationId": "string",
      "organizationName": "Ava Chen",
      "permissions": [
        "string"
      ],
      "profile": {},
      "userId": "string",
      "username": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `isAdmin` | boolean |  |
| `isTerminalUser` | boolean |  |
| `name` | string |  |
| `organizationId` | string |  |
| `organizationName` | string |  |
| `permissions` | array<string> |  |
| `profile` | object |  |
| `userId` | string |  |
| `username` | string |  |

## Native endpoint

Through the native snapADDY API, this operation is `GET /organization/v1/usernames` (base URL `https://api.snapaddy.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-organization-users.md) for the provider-specific parameters and requirements.

