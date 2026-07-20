# Salesmate: Get Active Users



```
GET https://connect.mindcloud.co/v1/universal/salesmate/latest/actions/get-active-users
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Salesmate `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/salesmate/latest/actions/get-active-users?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/salesmate/latest/actions/get-active-users?${params}`, {
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
      "createdAt": "2026-05-07T12:00:00.000Z",
      "dateFormat": "string",
      "email": "ava@example.com",
      "firstName": "Ava",
      "id": 1,
      "imagePath": "string",
      "isActive": 1,
      "isCurrentUser": true,
      "lastName": "Chen",
      "mobile": "string",
      "name": "Ava Chen",
      "photo": "string",
      "seats": [
        {}
      ],
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date | Creation timestamp. |
| `dateFormat` | string | Preferred date format. |
| `email` | string | User email address. |
| `firstName` | string | User first name. |
| `id` | number | Salesmate user ID. |
| `imagePath` | string | Image path. |
| `isActive` | number | Salesmate active flag. |
| `isCurrentUser` | boolean | Whether the user matches the connected account. |
| `lastName` | string | User last name. |
| `mobile` | string | User phone number. |
| `name` | string | Full user name. |
| `photo` | string | User photo URL or path. |
| `seats` | array<object> | Seat assignments. |
| `updatedAt` | date | Last update timestamp. |

## Native endpoint

Through the native Salesmate API, this operation is `GET /core/v4/users` (base URL `https://apis.salesmate.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-active-users.md) for the provider-specific parameters and requirements.

