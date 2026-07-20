# BigDataCloud: Get IPv4 Address Space Monitoring

Retrieves IPv4 address space monitoring data from BigDataCloud.

```
GET https://connect.mindcloud.co/v1/universal/bigDataCloud/latest/actions/get-ipv4-address-space-monitoring
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BigDataCloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bigDataCloud/latest/actions/get-ipv4-address-space-monitoring?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bigDataCloud/latest/actions/get-ipv4-address-space-monitoring?${params}`, {
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
      "bgpDataTimeStamp": "string",
      "distribution": [
        {}
      ],
      "registryDataTimeStamp": "string",
      "totalAddresses": 1,
      "totalAnnounced": 1,
      "totalBogon": 1,
      "updated": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `bgpDataTimeStamp` | string | BGP data timestamp in ISO 8601 format. |
| `distribution` | array<object> | Regional distribution of IPv4 address space data. |
| `registryDataTimeStamp` | string | Registry data timestamp in ISO 8601 format. |
| `totalAddresses` | number | Total IPv4 addresses included in the distribution. |
| `totalAnnounced` | number | Total BGP announced IPv4 addresses included in the distribution. |
| `totalBogon` | number | Total bogon IPv4 addresses announced in the distribution. |
| `updated` | string | Last updated timestamp in ISO 8601 format. |

## Native endpoint

Through the native BigDataCloud API, this operation is `GET /data/address-space-stats-ipv4` (base URL `https://api-bdc.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-ipv4-address-space-monitoring.md) for the provider-specific parameters and requirements.

