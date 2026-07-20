# Myphoner: Search Leads

Searches for leads in Myphoner by query.

```
GET https://connect.mindcloud.co/v1/universal/myphoner/latest/actions/search-leads
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Myphoner `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/myphoner/latest/actions/search-leads?connectionId=$CONNECTION_ID&limit=25&offset=0&query=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "query": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/myphoner/latest/actions/search-leads?${params}`, {
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
| `listIds` | string | no | Comma-separated list IDs to scope the search to specific lists. |
| `query` | string | yes | Free-text search query across lead data and activity logs. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "leads": [
        {
          "id": 1,
          "location": "string",
          "primaryIdentifier": "string",
          "state": "string",
          "url": "https://example.com"
        }
      ],
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `leads` | array<object> |  |
| `leads[].id` | number |  |
| `leads[].location` | string |  |
| `leads[].primaryIdentifier` | string |  |
| `leads[].state` | string |  |
| `leads[].url` | string |  |
| `total` | number |  |

## Native endpoint

Through the native Myphoner API, this operation is `GET /leads/search` (base URL `https://{{credentials.subdomain}}.myphoner.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/search-leads.md) for the provider-specific parameters and requirements.

