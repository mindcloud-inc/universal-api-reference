# CallPage: List Users

Retrieves all available users from CallPage.

```
GET https://connect.mindcloud.co/v1/universal/callPage/latest/actions/list-users
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CallPage `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/callPage/latest/actions/list-users?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/callPage/latest/actions/list-users?${params}`, {
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
      "activatedAt": "string",
      "avatar": {},
      "callerId": {
        "activatedAt": {},
        "id": 1,
        "updatedAt": "string"
      },
      "email": "ava@example.com",
      "id": 1,
      "lastOnline": {},
      "name": "Ava Chen",
      "parentId": {},
      "role": {
        "slug": "string"
      },
      "tel": "string",
      "telExtension": {},
      "telFormatted": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `activatedAt` | string |  |
| `avatar` | object |  |
| `callerId.activatedAt` | object |  |
| `callerId.id` | number |  |
| `callerId.updatedAt` | string |  |
| `email` | string |  |
| `id` | number |  |
| `lastOnline` | object |  |
| `name` | string |  |
| `parentId` | object |  |
| `role.slug` | string |  |
| `tel` | string |  |
| `telExtension` | object |  |
| `telFormatted` | string |  |

## Native endpoint

Through the native CallPage API, this operation is `GET /users/all` (base URL `https://core.callpage.io/api/v1/external`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-users.md) for the provider-specific parameters and requirements.

