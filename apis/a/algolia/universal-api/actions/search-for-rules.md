# Algolia: Search for Rules

Searches for rules in an Algolia index.

```
GET https://connect.mindcloud.co/v1/universal/algolia/latest/actions/search-for-rules
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Algolia `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/algolia/latest/actions/search-for-rules?connectionId=$CONNECTION_ID&indexName=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "indexName": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/algolia/latest/actions/search-for-rules?${params}`, {
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
| `indexName` | string | yes | Name of the index on which to search rules. |
| `query` | string | no | Text query to match rule object IDs or descriptions. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `anchoring` | string | no | Anchoring strategy for rule conditions. |
| `context` | string | no | Rule context to filter by. |
| `page` | number | no | Results page number. |
| `hitsPerPage` | number | no | Maximum number of rules to return. |
| `enabled` | boolean | no | Whether to return only enabled or disabled rules. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "hits": [
        {}
      ],
      "nbHits": 1,
      "nbPages": 1,
      "page": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `hits` | array<object> |  |
| `nbHits` | number |  |
| `nbPages` | number |  |
| `page` | number |  |

## Native endpoint

Through the native Algolia API, this operation is `POST /1/indexes/:indexName/rules/search` (base URL `https://{{credentials.applicationId}}.algolia.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-for-rules.md) for the provider-specific parameters and requirements.

