# ThingsBoard: Get Current User

Retrieves the current user from ThingsBoard.

```
GET https://connect.mindcloud.co/v1/universal/thingsBoard/latest/actions/get-current-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ThingsBoard `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/thingsBoard/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/thingsBoard/latest/actions/get-current-user?${params}`, {
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
      "authority": "string",
      "createdTime": 1,
      "email": "ava@example.com",
      "firstName": "Ava",
      "id": {
        "entityType": "string",
        "id": "string"
      },
      "lastName": "Chen",
      "name": "Ava Chen",
      "phone": "string",
      "tenantId": {
        "entityType": "string",
        "id": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `authority` | string |  |
| `createdTime` | number |  |
| `email` | string |  |
| `firstName` | string |  |
| `id.entityType` | string |  |
| `id.id` | string |  |
| `lastName` | string |  |
| `name` | string |  |
| `phone` | string |  |
| `tenantId.entityType` | string |  |
| `tenantId.id` | string |  |

## Native endpoint

Through the native ThingsBoard API, this operation is `GET /auth/user` (base URL `{{credentials.baseUrl}}/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-current-user.md) for the provider-specific parameters and requirements.

