# OneDeck: List Users

Retrieves a list of users from OneDeck.

```
GET https://connect.mindcloud.co/v1/universal/oneDeck/latest/actions/list-users
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OneDeck `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/oneDeck/latest/actions/list-users?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/oneDeck/latest/actions/list-users?${params}`, {
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
      "createDate": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "firstName": "Ava",
      "id": "string",
      "image": {},
      "isLanguageRtl": {},
      "lastName": "Chen",
      "role": "string",
      "status": "string",
      "twoFaEnabled": true,
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "username": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createDate` | date |  |
| `email` | string |  |
| `firstName` | string |  |
| `id` | string |  |
| `image` | object |  |
| `isLanguageRtl` | object |  |
| `lastName` | string |  |
| `role` | string |  |
| `status` | string |  |
| `twoFaEnabled` | boolean |  |
| `updatedAt` | date |  |
| `username` | object |  |

## Native endpoint

Through the native OneDeck API, this operation is `GET /users` (base URL `https://{{credentials.accountName}}.onedeck.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-users.md) for the provider-specific parameters and requirements.

