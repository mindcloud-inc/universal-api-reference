# BigDataCloud: Get Network by IP

Retrieves network details by IP address from BigDataCloud.

```
GET https://connect.mindcloud.co/v1/universal/bigDataCloud/latest/actions/get-network-by-ip
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BigDataCloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bigDataCloud/latest/actions/get-network-by-ip?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bigDataCloud/latest/actions/get-network-by-ip?${params}`, {
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
| `ip` | string | no | If omitted, BigDataCloud uses the caller IP address. Example: `44.221.74.44`. |
| `localityLanguage` | string | no | Preferred language for locality names in ISO 639-1 format. Default: `en`. Example: `en`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "bgpPrefix": "string",
      "bgpPrefixLastAddress": "string",
      "bgpPrefixNetworkAddress": "string",
      "carriers": [
        {
          "asn": "string",
          "asnNumeric": 1,
          "name": "Ava Chen",
          "organisation": "string",
          "rank": 1,
          "rankText": "string",
          "registeredCountry": "string",
          "registeredCountryName": "Ava Chen",
          "registrationLastChange": "2026-05-07T12:00:00.000Z",
          "registry": "string",
          "totalIpv4Addresses": 1,
          "totalIpv4BogonPrefixes": 1,
          "totalIpv4Prefixes": 1,
          "totalIpv6BogonPrefixes": 1,
          "totalIpv6Prefixes": 1
        }
      ],
      "ip": "string",
      "isBogon": true,
      "isReachableGlobally": true,
      "organisation": "string",
      "registeredCountry": "string",
      "registeredCountryName": "Ava Chen",
      "registry": "string",
      "registryStatus": "string",
      "totalAddresses": 1,
      "viaCarriers": [
        {
          "asn": "string",
          "asnNumeric": 1,
          "name": "Ava Chen",
          "organisation": "string",
          "rank": 1,
          "rankText": "string",
          "registeredCountry": "string",
          "registeredCountryName": "Ava Chen",
          "registry": "string",
          "totalIpv4Addresses": 1
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `bgpPrefix` | string |  |
| `bgpPrefixLastAddress` | string |  |
| `bgpPrefixNetworkAddress` | string |  |
| `carriers[].asn` | string |  |
| `carriers[].asnNumeric` | number |  |
| `carriers[].name` | string |  |
| `carriers[].organisation` | string |  |
| `carriers[].rank` | number |  |
| `carriers[].rankText` | string |  |
| `carriers[].registeredCountry` | string |  |
| `carriers[].registeredCountryName` | string |  |
| `carriers[].registrationLastChange` | date |  |
| `carriers[].registry` | string |  |
| `carriers[].totalIpv4Addresses` | number |  |
| `carriers[].totalIpv4BogonPrefixes` | number |  |
| `carriers[].totalIpv4Prefixes` | number |  |
| `carriers[].totalIpv6BogonPrefixes` | number |  |
| `carriers[].totalIpv6Prefixes` | number |  |
| `ip` | string |  |
| `isBogon` | boolean |  |
| `isReachableGlobally` | boolean |  |
| `organisation` | string |  |
| `registeredCountry` | string |  |
| `registeredCountryName` | string |  |
| `registry` | string |  |
| `registryStatus` | string |  |
| `totalAddresses` | number |  |
| `viaCarriers[].asn` | string |  |
| `viaCarriers[].asnNumeric` | number |  |
| `viaCarriers[].name` | string |  |
| `viaCarriers[].organisation` | string |  |
| `viaCarriers[].rank` | number |  |
| `viaCarriers[].rankText` | string |  |
| `viaCarriers[].registeredCountry` | string |  |
| `viaCarriers[].registeredCountryName` | string |  |
| `viaCarriers[].registry` | string |  |
| `viaCarriers[].totalIpv4Addresses` | number |  |

## Native endpoint

Through the native BigDataCloud API, this operation is `GET /data/network-by-ip` (base URL `https://api-bdc.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-network-by-ip.md) for the provider-specific parameters and requirements.

