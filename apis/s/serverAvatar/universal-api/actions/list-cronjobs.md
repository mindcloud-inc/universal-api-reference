# ServerAvatar: List Cronjobs

Retrieves cronjobs from ServerAvatar.

```
GET https://connect.mindcloud.co/v1/universal/serverAvatar/latest/actions/list-cronjobs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ServerAvatar `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/serverAvatar/latest/actions/list-cronjobs?connectionId=$CONNECTION_ID&organization=string&server=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "organization": "string",
  "server": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/serverAvatar/latest/actions/list-cronjobs?${params}`, {
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
      "cronjobs": {
        "currentPage": 1,
        "data": [
          {
            "command": "string",
            "createdAt": "string",
            "customScheduling": "string",
            "enabled": 1,
            "id": 1,
            "name": "Ava Chen",
            "schedule": "string",
            "serverId": 1,
            "systemUser": "string",
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
| `cronjobs` | object |  |
| `cronjobs.currentPage` | number |  |
| `cronjobs.data` | array<object> |  |
| `cronjobs.data[].command` | string |  |
| `cronjobs.data[].createdAt` | string |  |
| `cronjobs.data[].customScheduling` | string |  |
| `cronjobs.data[].enabled` | number |  |
| `cronjobs.data[].id` | number |  |
| `cronjobs.data[].name` | string |  |
| `cronjobs.data[].schedule` | string |  |
| `cronjobs.data[].serverId` | number |  |
| `cronjobs.data[].systemUser` | string |  |
| `cronjobs.data[].updatedAt` | string |  |
| `cronjobs.firstPageUrl` | string |  |
| `cronjobs.from` | number |  |
| `cronjobs.lastPage` | number |  |
| `cronjobs.lastPageUrl` | string |  |
| `cronjobs.links` | array<object> |  |
| `cronjobs.links[].active` | boolean |  |
| `cronjobs.links[].label` | string |  |
| `cronjobs.links[].url` | string |  |
| `cronjobs.nextPageUrl` | string |  |
| `cronjobs.path` | string |  |
| `cronjobs.perPage` | number |  |
| `cronjobs.prevPageUrl` | string |  |
| `cronjobs.to` | number |  |
| `cronjobs.total` | number |  |

## Native endpoint

Through the native ServerAvatar API, this operation is `GET /organizations/{{organization}}/servers/{{server}}/cronjobs` (base URL `https://api.serveravatar.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-cronjobs.md) for the provider-specific parameters and requirements.

