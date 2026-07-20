# Doctly: List Extractors



```
GET https://connect.mindcloud.co/v1/universal/doctly/latest/actions/list-extractors
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Doctly `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/doctly/latest/actions/list-extractors?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/doctly/latest/actions/list-extractors?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Doctly API returns.

## Native endpoint

Through the native Doctly API, this operation is `GET /e` (base URL `https://api.doctly.ai/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-extractors.md) for the provider-specific parameters and requirements.

