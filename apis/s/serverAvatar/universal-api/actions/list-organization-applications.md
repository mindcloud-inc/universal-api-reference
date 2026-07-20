# ServerAvatar: List Organization Applications

Retrieves organization applications from ServerAvatar.

```
GET https://connect.mindcloud.co/v1/universal/serverAvatar/latest/actions/list-organization-applications
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ServerAvatar `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/serverAvatar/latest/actions/list-organization-applications?connectionId=$CONNECTION_ID&organization=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "organization": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/serverAvatar/latest/actions/list-organization-applications?${params}`, {
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
      "applications": {
        "currentPage": 1,
        "data": [
          {}
        ],
        "firstPageUrl": "https://example.com",
        "from": "string",
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
        "to": "string",
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
| `applications.firstPageUrl` | string |  |
| `applications.from` | string |  |
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
| `applications.to` | string |  |
| `applications.total` | number |  |

## Native endpoint

Through the native ServerAvatar API, this operation is `GET /organizations/{{organization}}/applications` (base URL `https://api.serveravatar.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-organization-applications.md) for the provider-specific parameters and requirements.

