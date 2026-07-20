# Pilvio: Get Floating IP



```
GET https://connect.mindcloud.co/v1/universal/pilvio/latest/actions/get-floating-ip
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pilvio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pilvio/latest/actions/get-floating-ip?connectionId=$CONNECTION_ID&publicIpv4Address=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "publicIpv4Address": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pilvio/latest/actions/get-floating-ip?${params}`, {
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
| `publicIpv4Address` | string | yes | Public IPv4 address to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "address": "string",
      "billingAccountId": 1,
      "id": 1,
      "type": "string",
      "userId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address` | string |  |
| `billingAccountId` | number |  |
| `id` | number |  |
| `type` | string |  |
| `userId` | number |  |

## Native endpoint

Through the native Pilvio API, this operation is `GET /network/ip_addresses/{public_ipv4_address}` (base URL `https://api.pilvio.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-floating-ip.md) for the provider-specific parameters and requirements.

