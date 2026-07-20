# data.world: Execute a Saved Query

Executes a saved query in data.world.

```
GET https://connect.mindcloud.co/v1/universal/dataworld/latest/actions/execute-saved-query
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a data.world `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dataworld/latest/actions/execute-saved-query?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dataworld/latest/actions/execute-saved-query?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native data.world API returns.

## Native endpoint

Through the native data.world API, this operation is `GET /queries/{id}/results` (base URL `https://api.data.world/v0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/execute-saved-query.md) for the provider-specific parameters and requirements.

