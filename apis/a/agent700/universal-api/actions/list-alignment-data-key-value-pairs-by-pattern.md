# Agent700: List Alignment Data Key-Value Pairs by Pattern



```
GET https://connect.mindcloud.co/v1/universal/agent700/latest/actions/list-alignment-data-key-value-pairs-by-pattern
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Agent700 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/agent700/latest/actions/list-alignment-data-key-value-pairs-by-pattern?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/agent700/latest/actions/list-alignment-data-key-value-pairs-by-pattern?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Agent700 API returns.

## Native endpoint

Through the native Agent700 API, this operation is `GET /alignment-data/list-kv-by-pattern` (base URL `https://api.agent700.ai/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-alignment-data-key-value-pairs-by-pattern.md) for the provider-specific parameters and requirements.

