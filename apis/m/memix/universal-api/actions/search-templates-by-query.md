# Memix: Search Templates By Query

Finds templates in Memix by query.

```
GET https://connect.mindcloud.co/v1/universal/memix/latest/actions/search-templates-by-query
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Memix `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/memix/latest/actions/search-templates-by-query?connectionId=$CONNECTION_ID&q=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "q": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/memix/latest/actions/search-templates-by-query?${params}`, {
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
| `q` | string | yes | Search query for discovering templates. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `limit` | number | no | Maximum number of templates to return. Default: `50`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Memix API returns.

## Native endpoint

Through the native Memix API, this operation is `GET /v1/templates/search` (base URL `https://api.memix.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-templates-by-query.md) for the provider-specific parameters and requirements.

