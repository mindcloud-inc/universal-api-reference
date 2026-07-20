# ServerAvatar: List Organization Members

Retrieves organization members from ServerAvatar.

```
GET https://connect.mindcloud.co/v1/universal/serverAvatar/latest/actions/list-organization-members
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ServerAvatar `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/serverAvatar/latest/actions/list-organization-members?connectionId=$CONNECTION_ID&organization=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "organization": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/serverAvatar/latest/actions/list-organization-members?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `organization` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "members": {
        "currentPage": 1,
        "data": [
          {
            "createdAt": "string",
            "designation": "string",
            "email": "ava@example.com",
            "id": 1,
            "roles": [
              {
                "id": 1,
                "role": "string"
              }
            ],
            "updatedAt": "string",
            "user": {
              "avatar": "string",
              "email": "ava@example.com",
              "id": 1,
              "name": "Ava Chen"
            }
          }
        ],
        "firstPageUrl": "https://example.com",
        "from": 1,
        "lastPage": 1,
        "lastPageUrl": "https://example.com",
        "links": [
          {
            "active": true,
            "label": "https://example.com",
            "url": "https://example.com"
          }
        ],
        "nextPageUrl": "https://example.com",
        "path": "string",
        "perPage": 1,
        "prevPageUrl": "https://example.com",
        "to": 1,
        "total": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `members` | object |  |
| `members.currentPage` | number |  |
| `members.data` | array<object> |  |
| `members.data[].createdAt` | string |  |
| `members.data[].designation` | string |  |
| `members.data[].email` | string |  |
| `members.data[].id` | number |  |
| `members.data[].roles` | array<object> |  |
| `members.data[].roles[].id` | number |  |
| `members.data[].roles[].role` | string |  |
| `members.data[].updatedAt` | string |  |
| `members.data[].user` | object |  |
| `members.data[].user.avatar` | string |  |
| `members.data[].user.email` | string |  |
| `members.data[].user.id` | number |  |
| `members.data[].user.name` | string |  |
| `members.firstPageUrl` | string |  |
| `members.from` | number |  |
| `members.lastPage` | number |  |
| `members.lastPageUrl` | string |  |
| `members.links` | array<object> |  |
| `members.links[].active` | boolean |  |
| `members.links[].label` | string |  |
| `members.links[].url` | string |  |
| `members.nextPageUrl` | string |  |
| `members.path` | string |  |
| `members.perPage` | number |  |
| `members.prevPageUrl` | string |  |
| `members.to` | number |  |
| `members.total` | number |  |

## Native endpoint

Through the native ServerAvatar API, this operation is `GET /organizations/{{organization}}/members` (base URL `https://api.serveravatar.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-organization-members.md) for the provider-specific parameters and requirements.

