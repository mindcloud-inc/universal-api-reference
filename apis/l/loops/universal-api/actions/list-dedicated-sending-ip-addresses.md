# Loops: List Dedicated Sending IP Addresses

Retrieves dedicated sending IP addresses from Loops.

```
GET https://connect.mindcloud.co/v1/universal/loops/latest/actions/list-dedicated-sending-ip-addresses
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Loops `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/loops/latest/actions/list-dedicated-sending-ip-addresses?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/loops/latest/actions/list-dedicated-sending-ip-addresses?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "ipAddress": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ipAddress` | string | Dedicated sending IP address. |

## Native endpoint

Through the native Loops API, this operation is `GET /dedicated-sending-ips` (base URL `https://app.loops.so/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-dedicated-sending-ip-addresses.md) for the provider-specific parameters and requirements.

