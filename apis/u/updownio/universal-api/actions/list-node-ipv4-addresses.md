# updown.io: List Node IPv4 Addresses

Retrieves node IPv4 addresses from updown.io.

```
GET https://connect.mindcloud.co/v1/universal/updownio/latest/actions/list-node-ipv4-addresses
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a updown.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/updownio/latest/actions/list-node-ipv4-addresses?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/updownio/latest/actions/list-node-ipv4-addresses?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native updown.io API returns.

## Native endpoint

Through the native updown.io API, this operation is `GET /nodes/ipv4` (base URL `https://updown.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-node-ipv4-addresses.md) for the provider-specific parameters and requirements.

