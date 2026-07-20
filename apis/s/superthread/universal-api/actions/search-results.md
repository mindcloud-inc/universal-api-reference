# Superthread: Search Results



```
GET https://connect.mindcloud.co/v1/universal/superthread/latest/actions/search-results
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Superthread `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/superthread/latest/actions/search-results?connectionId=$CONNECTION_ID&limit=25&offset=0&query=string&teamId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "query": "string",
  "teamId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/superthread/latest/actions/search-results?${params}`, {
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
| `archived` | boolean | no | Include archived records in the search. |
| `fields` | string | no | Choose which fields Superthread should search. |
| `grouped` | boolean | no | Return grouped search results when enabled. |
| `projectId` | string | no | Limit results to one Superthread space or project. |
| `query` | string | yes | Search text to match across workspace content. |
| `statuses` | string | no | Limit card and epic search results to specific statuses. |
| `teamId` | string | yes | Workspace ID for the Superthread workspace to search. |
| `types` | string | no | Limit results to specific resource types. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "boards": [
        {}
      ],
      "cards": [
        {}
      ],
      "count": 1,
      "cursor": "string",
      "epics": [
        {}
      ],
      "notes": [
        {}
      ],
      "pages": [
        {}
      ],
      "projects": [
        {}
      ],
      "results": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `boards` | array<object> |  |
| `cards` | array<object> |  |
| `count` | number |  |
| `cursor` | string |  |
| `epics` | array<object> |  |
| `notes` | array<object> |  |
| `pages` | array<object> |  |
| `projects` | array<object> |  |
| `results` | array<object> |  |

## Native endpoint

Through the native Superthread API, this operation is `GET /:team_id/search` (base URL `https://api.superthread.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/search-results.md) for the provider-specific parameters and requirements.

