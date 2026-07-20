# ServerAvatar: List Server Applications

Retrieves server applications from ServerAvatar.

```
GET https://connect.mindcloud.co/v1/universal/serverAvatar/latest/actions/list-server-applications
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ServerAvatar `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/serverAvatar/latest/actions/list-server-applications?connectionId=$CONNECTION_ID&organization=string&server=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "organization": "string",
  "server": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/serverAvatar/latest/actions/list-server-applications?${params}`, {
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
      "applications": {
        "currentPage": 1,
        "data": [
          {
            "active": 1,
            "createdAt": "string",
            "createdByHumans": "string",
            "framework": "string",
            "id": 1,
            "name": "Ava Chen",
            "primaryDomain": "string",
            "serverId": 1,
            "size": 1,
            "ssl": "string",
            "updatedAt": "string"
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
| `applications` | object |  |
| `applications.currentPage` | number |  |
| `applications.data` | array<object> |  |
| `applications.data[].active` | number |  |
| `applications.data[].createdAt` | string |  |
| `applications.data[].createdByHumans` | string |  |
| `applications.data[].framework` | string |  |
| `applications.data[].id` | number |  |
| `applications.data[].name` | string |  |
| `applications.data[].primaryDomain` | string |  |
| `applications.data[].serverId` | number |  |
| `applications.data[].size` | number |  |
| `applications.data[].ssl` | string |  |
| `applications.data[].updatedAt` | string |  |
| `applications.firstPageUrl` | string |  |
| `applications.from` | number |  |
| `applications.lastPage` | number |  |
| `applications.lastPageUrl` | string |  |
| `applications.links` | array<object> |  |
| `applications.links[].active` | boolean |  |
| `applications.links[].label` | string |  |
| `applications.links[].url` | string |  |
| `applications.nextPageUrl` | string |  |
| `applications.path` | string |  |
| `applications.perPage` | number |  |
| `applications.prevPageUrl` | string |  |
| `applications.to` | number |  |
| `applications.total` | number |  |

## Native endpoint

Through the native ServerAvatar API, this operation is `GET /organizations/{{organization}}/servers/{{server}}/applications` (base URL `https://api.serveravatar.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-server-applications.md) for the provider-specific parameters and requirements.

