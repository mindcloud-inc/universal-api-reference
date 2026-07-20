# Histre: Search for Collections

Finds collections in Histre by search query.

```
GET https://connect.mindcloud.co/v1/universal/histre/latest/actions/search-collections
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Histre `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/histre/latest/actions/search-collections?connectionId=$CONNECTION_ID&q=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "q": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/histre/latest/actions/search-collections?${params}`, {
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
| `q` | string | yes | All or part of the collection title to search for. |
| `url` | string | no | Optional URL to include collection association information in the results. |
| `channel` | string | no | Optional request source channel. Histre docs allow extension or web. Default: `web`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Histre API returns.

## Native endpoint

Through the native Histre API, this operation is `GET /api/v1/collections/search/` (base URL `https://histre.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-collections.md) for the provider-specific parameters and requirements.

