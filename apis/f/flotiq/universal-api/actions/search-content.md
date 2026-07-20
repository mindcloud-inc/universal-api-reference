# Flotiq: Search Content

Searches content objects across your Flotiq project.

```
GET https://connect.mindcloud.co/v1/universal/flotiq/latest/actions/search-content
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Flotiq `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/flotiq/latest/actions/search-content?connectionId=$CONNECTION_ID&limit=25&offset=0&q=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "q": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/flotiq/latest/actions/search-content?${params}`, {
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
| `q` | string | yes | The search query string. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `content_type` | string | no | Optional content type name to scope search results. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Flotiq API returns.

## Native endpoint

Through the native Flotiq API, this operation is `GET /search` (base URL `https://api.flotiq.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/search-content.md) for the provider-specific parameters and requirements.

