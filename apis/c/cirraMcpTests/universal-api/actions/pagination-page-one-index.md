# Cirra MCP Tests - Do Not Delete: Pagination Page 1 Index



```
GET https://connect.mindcloud.co/v1/universal/cirraMcpTests/latest/actions/pagination-page-one-index
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cirra MCP Tests - Do Not Delete `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cirraMcpTests/latest/actions/pagination-page-one-index?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cirraMcpTests/latest/actions/pagination-page-one-index?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Cirra MCP Tests - Do Not Delete API returns.

## Native endpoint

Through the native Cirra MCP Tests - Do Not Delete API, this operation is `GET /pagination-t1-page-one-index` (base URL `https://api.mindcloud.co/v1/internal/cirra/tests`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/pagination-page-one-index.md) for the provider-specific parameters and requirements.

