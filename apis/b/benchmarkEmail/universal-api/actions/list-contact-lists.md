# Benchmark Email: List Contact Lists



```
GET https://connect.mindcloud.co/v1/universal/benchmarkEmail/latest/actions/list-contact-lists
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Benchmark Email `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/benchmarkEmail/latest/actions/list-contact-lists?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/benchmarkEmail/latest/actions/list-contact-lists?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Benchmark Email API returns.

## Native endpoint

Through the native Benchmark Email API, this operation is `GET /Contact/` (base URL `https://clientapi.benchmarkemail.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-contact-lists.md) for the provider-specific parameters and requirements.

