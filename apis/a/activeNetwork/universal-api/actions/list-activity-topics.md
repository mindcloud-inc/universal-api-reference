# Active Network: List Activity Topics

Finds activity topics in Active Network.

```
GET https://connect.mindcloud.co/v1/universal/activeNetwork/latest/actions/list-activity-topics
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Active Network `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/activeNetwork/latest/actions/list-activity-topics?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/activeNetwork/latest/actions/list-activity-topics?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Active Network API returns.

## Native endpoint

Through the native Active Network API, this operation is `GET /v2/search` (base URL `http://api.amp.active.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-activity-topics.md) for the provider-specific parameters and requirements.

