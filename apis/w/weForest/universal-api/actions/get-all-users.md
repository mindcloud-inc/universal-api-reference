# WeForest: Get all users

Retrieves all user records from WeForest.

```
GET https://connect.mindcloud.co/v1/universal/weForest/latest/actions/get-all-users
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WeForest `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/weForest/latest/actions/get-all-users?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/weForest/latest/actions/get-all-users?${params}`, {
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
      "customerId": 1,
      "email": "ava@example.com",
      "firstName": "Ava",
      "id": 1,
      "lastName": "Chen",
      "role": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `customerId` | number |  |
| `email` | string |  |
| `firstName` | string |  |
| `id` | number |  |
| `lastName` | string |  |
| `role` | string |  |

## Native endpoint

Through the native WeForest API, this operation is `GET /users` (base URL `https://api.weforest.org`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-all-users.md) for the provider-specific parameters and requirements.

