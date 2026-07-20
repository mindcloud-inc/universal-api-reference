# ServerAvatar: List Database Users

Retrieves database users from ServerAvatar.

```
GET https://connect.mindcloud.co/v1/universal/serverAvatar/latest/actions/list-database-users
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ServerAvatar `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/serverAvatar/latest/actions/list-database-users?connectionId=$CONNECTION_ID&organization=string&server=string&database=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "organization": "string",
  "server": "string",
  "database": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/serverAvatar/latest/actions/list-database-users?${params}`, {
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
| `database` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "databaseName": "Ava Chen",
      "databaseUsers": {
        "currentPage": 1,
        "data": [
          {
            "connectionPreference": "string",
            "createdAt": "string",
            "databaseId": 1,
            "hostname": [
              "Ava Chen"
            ],
            "id": 1,
            "mongodbRemoteIp": "string",
            "password": "string",
            "remoteAccess": true,
            "remoteIp": "string",
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
| `databaseName` | string |  |
| `databaseUsers` | object |  |
| `databaseUsers.currentPage` | number |  |
| `databaseUsers.data` | array<object> |  |
| `databaseUsers.data[].connectionPreference` | string |  |
| `databaseUsers.data[].createdAt` | string |  |
| `databaseUsers.data[].databaseId` | number |  |
| `databaseUsers.data[].hostname` | array<string> |  |
| `databaseUsers.data[].id` | number |  |
| `databaseUsers.data[].mongodbRemoteIp` | string |  |
| `databaseUsers.data[].password` | string |  |
| `databaseUsers.data[].remoteAccess` | boolean |  |
| `databaseUsers.data[].remoteIp` | string |  |
| `databaseUsers.data[].updatedAt` | string |  |
| `databaseUsers.data[].username` | string |  |
| `databaseUsers.firstPageUrl` | string |  |
| `databaseUsers.from` | number |  |
| `databaseUsers.lastPage` | number |  |
| `databaseUsers.lastPageUrl` | string |  |
| `databaseUsers.links` | array<object> |  |
| `databaseUsers.links[].active` | boolean |  |
| `databaseUsers.links[].label` | string |  |
| `databaseUsers.links[].url` | string |  |
| `databaseUsers.nextPageUrl` | string |  |
| `databaseUsers.path` | string |  |
| `databaseUsers.perPage` | number |  |
| `databaseUsers.prevPageUrl` | string |  |
| `databaseUsers.to` | number |  |
| `databaseUsers.total` | number |  |

## Native endpoint

Through the native ServerAvatar API, this operation is `GET /organizations/{{organization}}/servers/{{server}}/databases/{{database}}/database-users` (base URL `https://api.serveravatar.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-database-users.md) for the provider-specific parameters and requirements.

