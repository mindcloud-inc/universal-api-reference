# Box: Search Folders



```
GET https://connect.mindcloud.co/v1/universal/box/latest/actions/search-folders
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Box `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/box/latest/actions/search-folders?connectionId=$CONNECTION_ID&query=contracts" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "contracts"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/box/latest/actions/search-folders?${params}`, {
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
| `query` | string | yes | The text to search for in folder names and folder metadata. Example: `contracts`. |
| `limit` | number | no | Maximum number of folder search results to return. Example: `100`. |
| `offset` | number | no | Offset-based pagination start position for folder search results. Example: `0`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `ancestorFolderIds` | string | no | Optional comma-separated parent folder IDs to limit the search scope. Example: `0`. |
| `fields` | string | no | Optional comma-separated list of folder fields to include. Example: `id,type,name,path_collection`. |
| `sort` | string | no | Optional search sort field: relevance or modified_at. Example: `relevance`. |
| `direction` | string | no | Search sort direction: DESC or ASC. Example: `DESC`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "entries": [
        {}
      ],
      "limit": 1,
      "offset": 1,
      "total_count": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `entries` | array<object> | The folders returned by the search. |
| `limit` | number | The page size limit. |
| `offset` | number | The offset used for this page of folder search results. |
| `total_count` | number | The total number of matching folders available. |

## Native endpoint

Through the native Box API, this operation is `GET /search` (base URL `https://api.box.com/2.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-folders.md) for the provider-specific parameters and requirements.

