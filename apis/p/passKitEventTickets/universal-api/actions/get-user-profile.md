# PassKit Event Tickets: Get User Profile

Retrieves your user profile from PassKit.

```
GET https://connect.mindcloud.co/v1/universal/passKitEventTickets/latest/actions/get-user-profile
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PassKit Event Tickets `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/passKitEventTickets/latest/actions/get-user-profile?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/passKitEventTickets/latest/actions/get-user-profile?${params}`, {
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
      "companyId": "string",
      "companyName": "Ava Chen",
      "companyStatus": "string",
      "createdAt": "string",
      "email": "ava@example.com",
      "expiresAt": "string",
      "regionId": "string",
      "userId": "string",
      "username": "Ava Chen",
      "userPermissions": "string",
      "userStatus": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `companyId` | string |  |
| `companyName` | string |  |
| `companyStatus` | string |  |
| `createdAt` | string |  |
| `email` | string |  |
| `expiresAt` | string |  |
| `regionId` | string |  |
| `userId` | string |  |
| `username` | string |  |
| `userPermissions` | string |  |
| `userStatus` | string |  |

## Native endpoint

Through the native PassKit Event Tickets API, this operation is `GET /user/profile` (base URL `https://api.pub2.passkit.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-user-profile.md) for the provider-specific parameters and requirements.

