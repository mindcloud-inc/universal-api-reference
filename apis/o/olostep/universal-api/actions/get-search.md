# Olostep: Get Search

Retrieves details for a search in Olostep.

```
GET https://connect.mindcloud.co/v1/universal/olostep/latest/actions/get-search
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Olostep `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/olostep/latest/actions/get-search?connectionId=$CONNECTION_ID&searchId=search_123" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "searchId": "search_123"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/olostep/latest/actions/get-search?${params}`, {
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
| `searchId` | string | yes | The ID of the search to retrieve. Example: `search_123`. |

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

Through the native Olostep API, this operation is `GET /v1/searches/[:search_id]` (base URL `https://api.olostep.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-search.md) for the provider-specific parameters and requirements.

