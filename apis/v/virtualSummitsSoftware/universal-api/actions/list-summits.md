# Virtual Summits Software: List Summits



```
GET https://connect.mindcloud.co/v1/universal/virtualSummitsSoftware/latest/actions/list-summits
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Virtual Summits Software `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/virtualSummitsSoftware/latest/actions/list-summits?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/virtualSummitsSoftware/latest/actions/list-summits?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Virtual Summits Software API returns.

## Native endpoint

Through the native Virtual Summits Software API, this operation is `GET /summits` (base URL `https://api.virtualsummits.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-summits.md) for the provider-specific parameters and requirements.

