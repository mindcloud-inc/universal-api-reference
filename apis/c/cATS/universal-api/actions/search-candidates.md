# CATS: Search Candidates

Finds candidates in CATS by search query.

```
GET https://connect.mindcloud.co/v1/universal/cATS/latest/actions/search-candidates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CATS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cATS/latest/actions/search-candidates?connectionId=$CONNECTION_ID&query=MindCloud%20Tester" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "MindCloud Tester"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cATS/latest/actions/search-candidates?${params}`, {
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
| `query` | string | yes | The string to search within candidates for. Example: `MindCloud Tester`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native CATS API returns.

## Native endpoint

Through the native CATS API, this operation is `GET /candidates/search` (base URL `https://api.catsone.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-candidates.md) for the provider-specific parameters and requirements.

