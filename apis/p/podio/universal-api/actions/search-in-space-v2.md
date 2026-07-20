# Podio: Search in Space v2

Finds results in a Podio space.

```
GET https://connect.mindcloud.co/v1/universal/podio/latest/actions/search-in-space-v2
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Podio `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/podio/latest/actions/search-in-space-v2?connectionId=$CONNECTION_ID&limit=25&offset=0&spaceId=12345" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "spaceId": "12345"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/podio/latest/actions/search-in-space-v2?${params}`, {
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
| `spaceId` | string | yes | The ID of the space to search. Example: `12345`. |
| `query` | string | no | The text to search for. Example: `project kickoff`. |
| `refType` | list<string> | no | Restrict the search to a specific object type. One of: `app`, `conversation`, `file`, `item`, `profile`, `status`, `task`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `counts` | boolean | no | Return counts for each result type. |
| `highlights` | boolean | no | Return highlighted matches for each result. |
| `searchFields[]` | array<string> | no | The list of fields to search in. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "counts": {},
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
| `counts` | object |  |
| `results` | array<object> |  |

## Native endpoint

Through the native Podio API, this operation is `GET /search/space/:space_id/v2` (base URL `https://api.podio.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/search-in-space-v2.md) for the provider-specific parameters and requirements.

