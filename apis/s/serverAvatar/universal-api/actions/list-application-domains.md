# ServerAvatar: List Application Domains

Retrieves application domains from ServerAvatar.

```
GET https://connect.mindcloud.co/v1/universal/serverAvatar/latest/actions/list-application-domains
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ServerAvatar `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/serverAvatar/latest/actions/list-application-domains?connectionId=$CONNECTION_ID&organization=string&server=string&application=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "organization": "string",
  "server": "string",
  "application": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/serverAvatar/latest/actions/list-application-domains?${params}`, {
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
| `application` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "applicationDomains": {
        "currentPage": 1,
        "data": [
          {
            "autossl": 1,
            "createdAt": "string",
            "createdByHumans": "string",
            "dnsPropagation": 1,
            "domain": "string",
            "id": 1,
            "tempDomain": 1,
            "toggleTempDomain": 1
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
| `applicationDomains` | object |  |
| `applicationDomains.currentPage` | number |  |
| `applicationDomains.data` | array<object> |  |
| `applicationDomains.data[].autossl` | number |  |
| `applicationDomains.data[].createdAt` | string |  |
| `applicationDomains.data[].createdByHumans` | string |  |
| `applicationDomains.data[].dnsPropagation` | number |  |
| `applicationDomains.data[].domain` | string |  |
| `applicationDomains.data[].id` | number |  |
| `applicationDomains.data[].tempDomain` | number |  |
| `applicationDomains.data[].toggleTempDomain` | number |  |
| `applicationDomains.firstPageUrl` | string |  |
| `applicationDomains.from` | number |  |
| `applicationDomains.lastPage` | number |  |
| `applicationDomains.lastPageUrl` | string |  |
| `applicationDomains.links` | array<object> |  |
| `applicationDomains.links[].active` | boolean |  |
| `applicationDomains.links[].label` | string |  |
| `applicationDomains.links[].url` | string |  |
| `applicationDomains.nextPageUrl` | string |  |
| `applicationDomains.path` | string |  |
| `applicationDomains.perPage` | number |  |
| `applicationDomains.prevPageUrl` | string |  |
| `applicationDomains.to` | number |  |
| `applicationDomains.total` | number |  |

## Native endpoint

Through the native ServerAvatar API, this operation is `GET /organizations/{{organization}}/servers/{{server}}/applications/{{application}}/application-domains` (base URL `https://api.serveravatar.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-application-domains.md) for the provider-specific parameters and requirements.

