# DNSFilter: Get Network Counts



```
GET https://connect.mindcloud.co/v1/universal/dNSFilter/latest/actions/get-network-counts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DNSFilter `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dNSFilter/latest/actions/get-network-counts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dNSFilter/latest/actions/get-network-counts?${params}`, {
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
      "all": 1,
      "offline": 1,
      "protected": 1,
      "unprotected": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `all` | number |  |
| `offline` | number |  |
| `protected` | number |  |
| `unprotected` | number |  |

## Native endpoint

Through the native DNSFilter API, this operation is `GET /v1/networks/counts` (base URL `https://api.dnsfilter.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-network-counts.md) for the provider-specific parameters and requirements.

