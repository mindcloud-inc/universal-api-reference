# Cliengo: List Users



```
GET https://connect.mindcloud.co/v1/universal/cliengo/latest/actions/list-users
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cliengo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cliengo/latest/actions/list-users?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cliengo/latest/actions/list-users?${params}`, {
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
      "allowedWebsiteIds": [
        "string"
      ],
      "companyId": "string",
      "creationDate": "2026-05-07T12:00:00.000Z",
      "deletable": true,
      "deleted": true,
      "delighted": true,
      "email": "ava@example.com",
      "hashId": "string",
      "id": "string",
      "imageUrl": "https://example.com",
      "intercomHashId": "string",
      "isEmailVerified": true,
      "isSuperUser": true,
      "isTempPassword": true,
      "language": "string",
      "migrations": {},
      "mobileNotificationsSilenced": true,
      "name": "Ava Chen",
      "notificationsSilenced": true,
      "permissions": [
        "string"
      ],
      "phone": "string",
      "thumbnailUrl": "https://example.com",
      "tutorials": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `allowedWebsiteIds` | array<string> |  |
| `companyId` | string |  |
| `creationDate` | date |  |
| `deletable` | boolean |  |
| `deleted` | boolean |  |
| `delighted` | boolean |  |
| `email` | string |  |
| `hashId` | string |  |
| `id` | string |  |
| `imageUrl` | string |  |
| `intercomHashId` | string |  |
| `isEmailVerified` | boolean |  |
| `isSuperUser` | boolean |  |
| `isTempPassword` | boolean |  |
| `language` | string |  |
| `migrations` | object |  |
| `mobileNotificationsSilenced` | boolean |  |
| `name` | string |  |
| `notificationsSilenced` | boolean |  |
| `permissions` | array<string> |  |
| `phone` | string |  |
| `thumbnailUrl` | string |  |
| `tutorials` | array |  |

## Native endpoint

Through the native Cliengo API, this operation is `GET /users` (base URL `https://api.cliengo.com/1.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-users.md) for the provider-specific parameters and requirements.

