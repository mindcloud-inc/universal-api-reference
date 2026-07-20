# Mural: Get Current User

Retrieves the current user from Mural.

```
GET https://connect.mindcloud.co/v1/universal/mural/latest/actions/get-current-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mural `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mural/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mural/latest/actions/get-current-user?${params}`, {
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
      "avatar": "string",
      "createdOn": 1,
      "email": "ava@example.com",
      "firstName": "Ava",
      "id": "string",
      "lastActiveWorkspace": "string",
      "lastName": "Chen",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `avatar` | string |  |
| `createdOn` | number |  |
| `email` | string |  |
| `firstName` | string |  |
| `id` | string |  |
| `lastActiveWorkspace` | string |  |
| `lastName` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Mural API, this operation is `GET /users/me` (base URL `https://app.mural.co/api/public/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-current-user.md) for the provider-specific parameters and requirements.

