# Memix: Search Curated Templates

Finds curated templates in Memix search.

```
GET https://connect.mindcloud.co/v1/universal/memix/latest/actions/search-curated-templates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Memix `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/memix/latest/actions/search-curated-templates?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/memix/latest/actions/search-curated-templates?${params}`, {
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
| `q` | string | no | Optional query used to narrow curated templates. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `limit` | number | no | Maximum number of templates to return. Default: `50`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Memix API returns.

## Native endpoint

Through the native Memix API, this operation is `GET /v1/templates/search` (base URL `https://api.memix.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-curated-templates.md) for the provider-specific parameters and requirements.

