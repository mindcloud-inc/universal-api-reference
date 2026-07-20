# Olostep: Create Search

Creates a new search in Olostep.

```
POST https://connect.mindcloud.co/v1/universal/olostep/latest/actions/create-search
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Olostep `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/olostep/latest/actions/create-search" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "query": "best AI web scraping tools"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/olostep/latest/actions/create-search', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "query": "best AI web scraping tools"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `query` | string | yes | The search query to run. Example: `best AI web scraping tools`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "object": "string",
      "query": "string",
      "result": {
        "jsonContent": "string",
        "jsonHostedUrl": "https://example.com",
        "links": [
          {
            "description": "https://example.com",
            "title": "https://example.com",
            "url": "https://example.com"
          }
        ]
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created` | date |  |
| `id` | string |  |
| `object` | string |  |
| `query` | string |  |
| `result.jsonContent` | string |  |
| `result.jsonHostedUrl` | string |  |
| `result.links[].description` | string |  |
| `result.links[].title` | string |  |
| `result.links[].url` | string |  |

## Native endpoint

Through the native Olostep API, this operation is `POST /v1/searches` (base URL `https://api.olostep.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-search.md) for the provider-specific parameters and requirements.

