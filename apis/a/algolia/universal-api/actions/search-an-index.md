# Algolia: Search an Index

Searches one Algolia index for matching records.

```
GET https://connect.mindcloud.co/v1/universal/algolia/latest/actions/search-an-index
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Algolia `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/algolia/latest/actions/search-an-index?connectionId=$CONNECTION_ID&indexName=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "indexName": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/algolia/latest/actions/search-an-index?${params}`, {
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
| `indexName` | string | yes | The name of the Algolia index to search. |
| `params` | string | no | URL-encoded Algolia search parameters. Example: `query=Wizard&hitsPerPage=5`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "hits": [
        {}
      ],
      "hitsPerPage": 1,
      "nbHits": 1,
      "nbPages": 1,
      "page": 1,
      "params": "string",
      "processingTimeMS": 1,
      "query": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `hits` | array<object> |  |
| `hitsPerPage` | number |  |
| `nbHits` | number |  |
| `nbPages` | number |  |
| `page` | number |  |
| `params` | string |  |
| `processingTimeMS` | number |  |
| `query` | string |  |

## Native endpoint

Through the native Algolia API, this operation is `POST /1/indexes/:indexName/query` (base URL `https://{{credentials.applicationId}}.algolia.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-an-index.md) for the provider-specific parameters and requirements.

