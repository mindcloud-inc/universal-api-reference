# KLIPY: Get Search Suggestions

Retrieves search suggestions from KLIPY for a query.

```
GET https://connect.mindcloud.co/v1/universal/kLIPY/latest/actions/get-search-suggestions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a KLIPY `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kLIPY/latest/actions/get-search-suggestions?connectionId=$CONNECTION_ID&query=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kLIPY/latest/actions/get-search-suggestions?${params}`, {
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
| `query` | string | yes |  |
| `limit` | number | no | Default: `10`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native KLIPY API returns.

## Native endpoint

Through the native KLIPY API, this operation is `GET /api/v1/:app_key/search-suggestions/:q` (base URL `https://api.klipy.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-search-suggestions.md) for the provider-specific parameters and requirements.

