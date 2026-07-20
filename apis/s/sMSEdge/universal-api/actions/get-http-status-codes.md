# SMSEdge: Get HTTP Status Codes

Retrieves HTTP status codes from SMSEdge.

```
GET https://connect.mindcloud.co/v1/universal/sMSEdge/latest/actions/get-http-status-codes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SMSEdge `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sMSEdge/latest/actions/get-http-status-codes?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sMSEdge/latest/actions/get-http-status-codes?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native SMSEdge API returns.

## Native endpoint

Through the native SMSEdge API, this operation is `POST /references/statuses/` (base URL `https://api.smsedge.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-http-status-codes.md) for the provider-specific parameters and requirements.

