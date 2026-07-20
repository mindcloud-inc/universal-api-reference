# IP2Proxy: Get Proxy Lookup

Retrieves proxy details for an IP address from IP2Proxy.

```
GET https://connect.mindcloud.co/v1/universal/iP2Proxy/latest/actions/get-proxy-lookup
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a IP2Proxy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/iP2Proxy/latest/actions/get-proxy-lookup?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/iP2Proxy/latest/actions/get-proxy-lookup?${params}`, {
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
| `ip` | string | no | Public IPv4 or IPv6 address to look up. Default: `201.42.237.89`. |
| `package` | string | no | IP2Proxy package tier to query. Default: `PX11`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native IP2Proxy API returns.

## Native endpoint

Through the native IP2Proxy API, this operation is `GET /` (base URL `https://api.ip2proxy.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-proxy-lookup.md) for the provider-specific parameters and requirements.

