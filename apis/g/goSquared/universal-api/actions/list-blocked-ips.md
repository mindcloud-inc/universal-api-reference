# GoSquared: List Blocked IPs

Retrieves blocked IP addresses from GoSquared.

```
GET https://connect.mindcloud.co/v1/universal/goSquared/latest/actions/list-blocked-ips
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GoSquared `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/goSquared/latest/actions/list-blocked-ips?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/goSquared/latest/actions/list-blocked-ips?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native GoSquared API returns.

## Native endpoint

Through the native GoSquared API, this operation is `GET account/v1/blocked/ips` (base URL `https://api.gosquared.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-blocked-ips.md) for the provider-specific parameters and requirements.

