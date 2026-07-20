# 1001fx: Search JSON

Finds matching key-value pairs in a JSON object.

```
GET https://connect.mindcloud.co/v1/universal/fx/latest/actions/search-json
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a 1001fx `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fx/latest/actions/search-json?connectionId=$CONNECTION_ID&comparison=string&searchString=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "comparison": "string",
  "searchString": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fx/latest/actions/search-json?${params}`, {
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
| `comparison` | string | yes | Comparison mode used for the search. |
| `json` | object | no | JSON object to search. |
| `jsonString` | string | no | JSON string to search when not passing a JSON object. |
| `scope` | string | no | Scope to search within. |
| `searchString` | string | yes | String to search for in the JSON payload. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native 1001fx API returns.

## Native endpoint

Through the native 1001fx API, this operation is `POST /data/deepsearchjson` (base URL `https://api.1001fx.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-json.md) for the provider-specific parameters and requirements.

