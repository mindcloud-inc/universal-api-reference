# Markup AI: List Term Sets

Retrieves term sets from Markup AI.

```
GET https://connect.mindcloud.co/v1/universal/markupAI/latest/actions/list-term-sets
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Markup AI `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/markupAI/latest/actions/list-term-sets?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/markupAI/latest/actions/list-term-sets?${params}`, {
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
| `searchTerm` | string | no | Optional text used to filter term sets. |
| `domainIds[]` | array<string> | no | Optional terminology domain IDs to restrict listed term sets. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "page": 1,
      "page_size": 1,
      "term_sets": [
        {}
      ],
      "total_count": 1,
      "total_pages": 1,
      "total_unfiltered_term_sets": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `page` | number |  |
| `page_size` | number |  |
| `term_sets` | array<object> |  |
| `total_count` | number |  |
| `total_pages` | number |  |
| `total_unfiltered_term_sets` | number |  |

## Native endpoint

Through the native Markup AI API, this operation is `GET /v1/terminology/term-sets` (base URL `https://api.markup.ai`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-term-sets.md) for the provider-specific parameters and requirements.

