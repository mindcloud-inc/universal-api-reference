# ACLU: Search Nodes

Finds Torture Database nodes by keyword and filters.

```
GET https://connect.mindcloud.co/v1/universal/aCLU/latest/actions/search-nodes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ACLU `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/aCLU/latest/actions/search-nodes?connectionId=$CONNECTION_ID&keys=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "keys": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/aCLU/latest/actions/search-nodes?${params}`, {
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
| `keys` | string | yes | Search keywords exactly as documented. |
| `page` | number | no | Zero-based page number. Default: `0`. |
| `filters` | string | no | Raw Solr filter string copied from the site URL after filters=. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "date": 1,
      "fields": {},
      "link": "https://example.com",
      "score": 1,
      "snippet": "string",
      "title": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `date` | number |  |
| `fields` | object |  |
| `link` | string |  |
| `score` | number |  |
| `snippet` | string |  |
| `title` | string |  |
| `type` | string |  |

## Native endpoint

Through the native ACLU API, this operation is `GET /searchnode/retrieve.json` (base URL `https://www.thetorturedatabase.org/rest`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-nodes.md) for the provider-specific parameters and requirements.

