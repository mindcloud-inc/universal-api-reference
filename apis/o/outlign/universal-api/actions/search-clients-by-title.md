# Outlign: Search Clients By Title

Finds clients in Outlign by title.

```
GET https://connect.mindcloud.co/v1/universal/outlign/latest/actions/search-clients-by-title
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Outlign `connectionId` ([setup](../authentication.md)).

This action also supports [filtering](../filtering.md) (`where`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/outlign/latest/actions/search-clients-by-title?connectionId=$CONNECTION_ID&title=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "title": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/outlign/latest/actions/search-clients-by-title?${params}`, {
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
| `title` | string | yes | Filter clients by title using partial match |
| `perPage` | number | no | Number of results per page (max 1000) |

## Response

```json
{
  "success": true,
  "data": [
    {
      "links": {
        "first": "https://example.com",
        "last": {},
        "next": {},
        "prev": {}
      },
      "meta": {
        "currentPage": 1,
        "currentPageUrl": "https://example.com",
        "from": {},
        "path": "string",
        "perPage": 1,
        "to": {}
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `links.first` | string |  |
| `links.last` | object |  |
| `links.next` | object |  |
| `links.prev` | object |  |
| `meta.currentPage` | number |  |
| `meta.currentPageUrl` | string |  |
| `meta.from` | object |  |
| `meta.path` | string |  |
| `meta.perPage` | number |  |
| `meta.to` | object |  |

## Native endpoint

Through the native Outlign API, this operation is `GET /clients` (base URL `https://go.outlign.co/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-clients-by-title.md) for the provider-specific parameters and requirements.

