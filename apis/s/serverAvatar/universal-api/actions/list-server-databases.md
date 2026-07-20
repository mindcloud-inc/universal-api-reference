# ServerAvatar: List Server Databases

Retrieves server databases from ServerAvatar.

```
GET https://connect.mindcloud.co/v1/universal/serverAvatar/latest/actions/list-server-databases
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ServerAvatar `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/serverAvatar/latest/actions/list-server-databases?connectionId=$CONNECTION_ID&organization=string&server=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "organization": "string",
  "server": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/serverAvatar/latest/actions/list-server-databases?${params}`, {
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
      "databases": {
        "currentPage": 1,
        "data": [
          {
            "agentStatus": "string",
            "automaticBackup": 1,
            "countryCode": "string",
            "createdAt": "string",
            "createdByHumans": "string",
            "databaseType": "string",
            "deletedAt": "string",
            "host": "string",
            "id": 1,
            "name": "Ava Chen",
            "remoteAccess": true,
            "serverId": 1,
            "serverName": "Ava Chen",
            "size": 1,
            "updatedAt": "string",
            "usersCount": 1
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
| `databases` | object |  |
| `databases.currentPage` | number |  |
| `databases.data` | array<object> |  |
| `databases.data[].agentStatus` | string |  |
| `databases.data[].automaticBackup` | number |  |
| `databases.data[].countryCode` | string |  |
| `databases.data[].createdAt` | string |  |
| `databases.data[].createdByHumans` | string |  |
| `databases.data[].databaseType` | string |  |
| `databases.data[].deletedAt` | string |  |
| `databases.data[].host` | string |  |
| `databases.data[].id` | number |  |
| `databases.data[].name` | string |  |
| `databases.data[].remoteAccess` | boolean |  |
| `databases.data[].serverId` | number |  |
| `databases.data[].serverName` | string |  |
| `databases.data[].size` | number |  |
| `databases.data[].updatedAt` | string |  |
| `databases.data[].usersCount` | number |  |
| `databases.firstPageUrl` | string |  |
| `databases.from` | number |  |
| `databases.lastPage` | number |  |
| `databases.lastPageUrl` | string |  |
| `databases.links` | array<object> |  |
| `databases.links[].active` | boolean |  |
| `databases.links[].label` | string |  |
| `databases.links[].url` | string |  |
| `databases.nextPageUrl` | string |  |
| `databases.path` | string |  |
| `databases.perPage` | number |  |
| `databases.prevPageUrl` | string |  |
| `databases.to` | number |  |
| `databases.total` | number |  |

## Native endpoint

Through the native ServerAvatar API, this operation is `GET /organizations/{{organization}}/servers/{{server}}/databases` (base URL `https://api.serveravatar.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-server-databases.md) for the provider-specific parameters and requirements.

