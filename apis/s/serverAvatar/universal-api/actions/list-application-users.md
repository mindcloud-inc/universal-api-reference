# ServerAvatar: List Application Users

Retrieves application users from ServerAvatar.

```
GET https://connect.mindcloud.co/v1/universal/serverAvatar/latest/actions/list-application-users
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ServerAvatar `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/serverAvatar/latest/actions/list-application-users?connectionId=$CONNECTION_ID&organization=string&server=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "organization": "string",
  "server": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/serverAvatar/latest/actions/list-application-users?${params}`, {
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
| `server` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "systemUsers": {
        "currentPage": 1,
        "data": [
          {
            "applications": [
              {}
            ],
            "createdAt": "string",
            "deletedAt": "string",
            "group": "string",
            "id": 1,
            "password": "string",
            "publicKey": "string",
            "rootAccess": 1,
            "serverId": 1,
            "sshAccess": true,
            "updatedAt": "string",
            "username": "Ava Chen"
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
| `systemUsers` | object |  |
| `systemUsers.currentPage` | number |  |
| `systemUsers.data` | array<object> |  |
| `systemUsers.data[].applications` | array<object> |  |
| `systemUsers.data[].createdAt` | string |  |
| `systemUsers.data[].deletedAt` | string |  |
| `systemUsers.data[].group` | string |  |
| `systemUsers.data[].id` | number |  |
| `systemUsers.data[].password` | string |  |
| `systemUsers.data[].publicKey` | string |  |
| `systemUsers.data[].rootAccess` | number |  |
| `systemUsers.data[].serverId` | number |  |
| `systemUsers.data[].sshAccess` | boolean |  |
| `systemUsers.data[].updatedAt` | string |  |
| `systemUsers.data[].username` | string |  |
| `systemUsers.firstPageUrl` | string |  |
| `systemUsers.from` | number |  |
| `systemUsers.lastPage` | number |  |
| `systemUsers.lastPageUrl` | string |  |
| `systemUsers.links` | array<object> |  |
| `systemUsers.links[].active` | boolean |  |
| `systemUsers.links[].label` | string |  |
| `systemUsers.links[].url` | string |  |
| `systemUsers.nextPageUrl` | string |  |
| `systemUsers.path` | string |  |
| `systemUsers.perPage` | number |  |
| `systemUsers.prevPageUrl` | string |  |
| `systemUsers.to` | number |  |
| `systemUsers.total` | number |  |

## Native endpoint

Through the native ServerAvatar API, this operation is `GET /organizations/{{organization}}/servers/{{server}}/system-users` (base URL `https://api.serveravatar.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-application-users.md) for the provider-specific parameters and requirements.

