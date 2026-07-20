# BigDataCloud: List BGP Active Prefixes

Retrieves active BGP prefixes from BigDataCloud.

```
GET https://connect.mindcloud.co/v1/universal/bigDataCloud/latest/actions/list-bgp-active-prefixes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BigDataCloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bigDataCloud/latest/actions/list-bgp-active-prefixes?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bigDataCloud/latest/actions/list-bgp-active-prefixes?${params}`, {
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
| `bogonsOnly` | boolean | no | Limit the response to bogon routes only. Default: `false`. Example: `false`. |
| `batchSize` | number | no | Requested batch size. Maximum value is 1000. Example: `10`. |
| `offset` | number | no | Number of entries to skip. Default: `0`. Example: `0`. |
| `sort` | string | no | Sort by bgpPrefix, bgpPrefixNetworkAddress, bgpPrefixLastAddress, registryStatus, isBogon, isAnnounced, or carriers. Default: `bgpPrefixNetworkAddress`. Example: `bgpPrefixNetworkAddress`. |
| `order` | string | no | Sort order: asc or desc. Default: `asc`. Example: `asc`. |
| `asn` | string | no | Autonomous System Number as numeric or ASN format. Example: `AS14618`. |
| `localityLanguage` | string | no | Preferred language for localized country names. Default: `en`. Example: `en`. |
| `isv4` | boolean | no | When false, the response lists IPv6 prefixes. If omitted, IPv4 is assumed. Example: `true`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "batch": 1,
      "offset": 1,
      "prefixes": [
        {}
      ],
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `batch` | number | Number of entries in the current batch. |
| `offset` | number | Number of entries skipped in the result. |
| `prefixes` | array<object> | Array of prefix entries returned for the current batch. |
| `total` | number | Total prefixes found. |

## Native endpoint

Through the native BigDataCloud API, this operation is `GET /data/prefixes-list` (base URL `https://api-bdc.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-bgp-active-prefixes.md) for the provider-specific parameters and requirements.

