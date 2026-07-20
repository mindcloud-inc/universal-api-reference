# Copperx: Get Current User

Retrieves the current user from Copperx.

```
GET https://connect.mindcloud.co/v1/universal/copperx/latest/actions/get-current-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Copperx `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/copperx/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/copperx/latest/actions/get-current-user?${params}`, {
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
      "accountType": "string",
      "address": {},
      "createdAt": "string",
      "email": "ava@example.com",
      "firstName": "Ava",
      "flags": {},
      "id": "string",
      "lastName": "Chen",
      "organization": {},
      "phone": "string",
      "position": "string",
      "profilePicture": "string",
      "role": "string",
      "status": "string",
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountType` | string |  |
| `address` | object |  |
| `createdAt` | string |  |
| `email` | string |  |
| `firstName` | string |  |
| `flags` | object |  |
| `id` | string |  |
| `lastName` | string |  |
| `organization` | object |  |
| `phone` | string |  |
| `position` | string |  |
| `profilePicture` | string |  |
| `role` | string |  |
| `status` | string |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native Copperx API, this operation is `GET /auth/me` (base URL `https://api.copperx.dev/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-current-user.md) for the provider-specific parameters and requirements.

