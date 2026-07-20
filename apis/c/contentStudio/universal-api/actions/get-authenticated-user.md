# ContentStudio: Get Authenticated User

Retrieves the authenticated user from ContentStudio.

```
GET https://connect.mindcloud.co/v1/universal/contentStudio/latest/actions/get-authenticated-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ContentStudio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/contentStudio/latest/actions/get-authenticated-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/contentStudio/latest/actions/get-authenticated-user?${params}`, {
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
      "authenticatedAt": "2026-05-07T12:00:00.000Z",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "dateFormat": "string",
      "email": "ava@example.com",
      "firstname": "Ava",
      "fullName": "Ava Chen",
      "Id": "string",
      "image": "string",
      "lastname": "Chen",
      "phoneNo": "string",
      "state": "string",
      "timeFormat": "string",
      "username": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `authenticatedAt` | date |  |
| `createdAt` | date |  |
| `dateFormat` | string |  |
| `email` | string |  |
| `firstname` | string |  |
| `fullName` | string |  |
| `Id` | string |  |
| `image` | string |  |
| `lastname` | string |  |
| `phoneNo` | string |  |
| `state` | string |  |
| `timeFormat` | string |  |
| `username` | string |  |

## Native endpoint

Through the native ContentStudio API, this operation is `GET /me` (base URL `https://api.contentstudio.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-authenticated-user.md) for the provider-specific parameters and requirements.

