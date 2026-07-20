# Histre: Search for Highlights

Finds highlights in Histre by search query.

```
GET https://connect.mindcloud.co/v1/universal/histre/latest/actions/search-highlights
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Histre `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/histre/latest/actions/search-highlights?connectionId=$CONNECTION_ID&q=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "q": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/histre/latest/actions/search-highlights?${params}`, {
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
| `q` | string | yes | Search query used to find matching highlights. |
| `url` | string | no | Optional page URL to scope highlight search. |
| `page` | number | no | Optional page number for paginated highlight search results. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Histre API returns.

## Native endpoint

Through the native Histre API, this operation is `GET /api/v1/highlight/` (base URL `https://histre.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-highlights.md) for the provider-specific parameters and requirements.

