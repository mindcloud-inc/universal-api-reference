# Exa: Create Webset Search

Creates a new webset search in Exa.

```
POST https://connect.mindcloud.co/v1/universal/exa/latest/actions/create-webset-search
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Exa `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/exa/latest/actions/create-webset-search" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "webset": "string",
  "count": 1,
  "query": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/exa/latest/actions/create-webset-search', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "webset": "string",
    "count": 1,
    "query": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `webset` | string | yes | The id of the Webset |
| `count` | number | yes | Number of Items the Search will attempt to find. The actual number of Items found may be less than this number depending on the query complexity. |
| `query` | string | yes | Natural language search query describing what you are looking for. Be specific and descriptive about your requirements, characteristics, and any constraints that help narrow down the results. Any URLs provided will be crawled and used as additional context for the search. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `entity.type` | string | no | Default: `custom`. |
| `entity.description` | string | no |  |
| `criteria` | string | no | Criteria every item is evaluated against. It's not required to provide your own criteria, we automatically detect the criteria from all the information provided in the query. Only use this when you need more fine control. |
| `exclude` | string | no | Sources (existing imports or websets) to exclude from search results. Any results found within these sources will be omitted to prevent finding them during search. |
| `scope` | string | no | Limit the search to specific sources (existing imports). Any results found within these sources matching the search criteria will be included in the Webset. |
| `recall` | string | no | Whether to provide an estimate of how many total relevant results could exist for this search. Result of the analysis will be available in the `recall` field within the search request. |
| `behavior` | string | no |  |
| `metadata` | string | no | Set of key-value pairs you want to associate with this object. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "behavior": "string",
      "canceledAt": "string",
      "canceledReason": "string",
      "count": "string",
      "createdAt": "string",
      "criteria": "string",
      "entity": {
        "description": "string",
        "type": "string"
      },
      "exclude": "string",
      "id": "string",
      "metadata": "string",
      "object": "string",
      "progress": {
        "analyzed": "string",
        "completion": "string",
        "found": "string",
        "timeLeft": "string"
      },
      "query": "string",
      "recall": {},
      "scope": "string",
      "status": "string",
      "updatedAt": "string",
      "websetId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `behavior` | string |  |
| `canceledAt` | string |  |
| `canceledReason` | string |  |
| `count` | string |  |
| `createdAt` | string |  |
| `criteria` | string |  |
| `entity` | object |  |
| `entity.description` | string |  |
| `entity.type` | string |  |
| `exclude` | string |  |
| `id` | string |  |
| `metadata` | string |  |
| `object` | string |  |
| `progress` | object |  |
| `progress.analyzed` | string |  |
| `progress.completion` | string |  |
| `progress.found` | string |  |
| `progress.timeLeft` | string |  |
| `query` | string |  |
| `recall` | object |  |
| `scope` | string |  |
| `status` | string |  |
| `updatedAt` | string |  |
| `websetId` | string |  |

## Native endpoint

Through the native Exa API, this operation is `POST /websets/v0/websets/:webset/searches` (base URL `https://api.exa.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-webset-search.md) for the provider-specific parameters and requirements.

