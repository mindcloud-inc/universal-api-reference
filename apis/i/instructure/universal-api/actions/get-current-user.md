# Instructure: Get Current User

Retrieves the current user from Instructure Canvas.

```
GET https://connect.mindcloud.co/v1/universal/instructure/latest/actions/get-current-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Instructure `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/instructure/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/instructure/latest/actions/get-current-user?${params}`, {
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
      "avatarUrl": "https://example.com",
      "createdAt": "string",
      "effectiveLocale": "string",
      "firstName": "Ava",
      "id": 1,
      "lastName": "Chen",
      "locale": "string",
      "name": "Ava Chen",
      "permissions": {},
      "shortName": "Ava Chen",
      "sortableName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `avatarUrl` | string |  |
| `createdAt` | string |  |
| `effectiveLocale` | string |  |
| `firstName` | string |  |
| `id` | number |  |
| `lastName` | string |  |
| `locale` | string |  |
| `name` | string |  |
| `permissions` | object |  |
| `shortName` | string |  |
| `sortableName` | string |  |

## Native endpoint

Through the native Instructure API, this operation is `GET /users/self` (base URL `https://canvas.instructure.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-current-user.md) for the provider-specific parameters and requirements.

