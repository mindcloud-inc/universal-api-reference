# Ecwid: Search Categories by Path

Finds categories in Ecwid by path.

```
GET https://connect.mindcloud.co/v1/universal/ecwid/latest/actions/search-categories-by-path
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ecwid `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ecwid/latest/actions/search-categories-by-path?connectionId=$CONNECTION_ID&path=string&delimeter=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "path": "string",
  "delimeter": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ecwid/latest/actions/search-categories-by-path?${params}`, {
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
| `path` | string | yes | Category path to resolve. |
| `delimeter` | string | yes | Path segment delimiter. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Ecwid API returns.

## Native endpoint

Through the native Ecwid API, this operation is `GET /:storeId/categoriesByPath` (base URL `https://app.ecwid.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-categories-by-path.md) for the provider-specific parameters and requirements.

