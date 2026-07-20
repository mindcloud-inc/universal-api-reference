# ServerAvatar: List Organizations

Retrieves organizations from ServerAvatar.

```
GET https://connect.mindcloud.co/v1/universal/serverAvatar/latest/actions/list-organizations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ServerAvatar `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/serverAvatar/latest/actions/list-organizations?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/serverAvatar/latest/actions/list-organizations?${params}`, {
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
      "organizations": [
        {
          "createdAt": "string",
          "id": 1,
          "members": [
            {
              "avatar": "string",
              "email": "ava@example.com",
              "name": "Ava Chen",
              "roles": [
                {
                  "id": 1,
                  "role": "string"
                }
              ]
            }
          ],
          "name": "Ava Chen"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `organizations` | array<object> |  |
| `organizations[].createdAt` | string |  |
| `organizations[].id` | number |  |
| `organizations[].members` | array<object> |  |
| `organizations[].members[].avatar` | string |  |
| `organizations[].members[].email` | string |  |
| `organizations[].members[].name` | string |  |
| `organizations[].members[].roles` | array<object> |  |
| `organizations[].members[].roles[].id` | number |  |
| `organizations[].members[].roles[].role` | string |  |
| `organizations[].name` | string |  |

## Native endpoint

Through the native ServerAvatar API, this operation is `GET /organizations` (base URL `https://api.serveravatar.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-organizations.md) for the provider-specific parameters and requirements.

