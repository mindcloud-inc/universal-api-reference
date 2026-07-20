# Pilvio: List Networks



```
GET https://connect.mindcloud.co/v1/universal/pilvio/latest/actions/list-networks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pilvio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pilvio/latest/actions/list-networks?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pilvio/latest/actions/list-networks?${params}`, {
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
      "createdAt": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "subnet": "string",
      "subnetIpv6": "string",
      "vlanId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `name` | string |  |
| `subnet` | string |  |
| `subnetIpv6` | string |  |
| `vlanId` | number |  |

## Native endpoint

Through the native Pilvio API, this operation is `GET /network/networks` (base URL `https://api.pilvio.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-networks.md) for the provider-specific parameters and requirements.

