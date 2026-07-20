# BigDataCloud: Get ASN Receiving From

Retrieves ASN receiving-from information from BigDataCloud.

```
GET https://connect.mindcloud.co/v1/universal/bigDataCloud/latest/actions/get-asn-receiving-from
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BigDataCloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bigDataCloud/latest/actions/get-asn-receiving-from?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bigDataCloud/latest/actions/get-asn-receiving-from?${params}`, {
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
| `asn` | string | no | Autonomous System Number as numeric or ASN format. Example: `AS14618`. |
| `batchSize` | number | no | Number of receivingFrom entries to retrieve. Hard limit is 50. Example: `10`. |
| `offset` | number | no | Number of receivingFrom entries to skip. Default: `0`. Example: `0`. |
| `localityLanguage` | string | no | Preferred language for localized country names. Default: `en`. Example: `en`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "asn": "string",
      "asnNumeric": 1,
      "name": "Ava Chen",
      "organisation": "string",
      "rank": 1,
      "rankText": "string",
      "receivingFrom": [
        {}
      ],
      "registeredCountry": "string",
      "registeredCountryName": "Ava Chen",
      "registrationLastChange": "string",
      "registry": "string",
      "totalIpv4Addresses": 1,
      "totalIpv4BogonPrefixes": 1,
      "totalIpv4Prefixes": 1,
      "totalIpv6BogonPrefixes": 1,
      "totalIpv6Prefixes": 1,
      "totalReceivingFrom": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `asn` | string | Autonomous System Number string. |
| `asnNumeric` | number | Autonomous System Number. |
| `name` | string | Registered ASN name. |
| `organisation` | string | Registered organization. |
| `rank` | number | Global rank by total number of announced IP addresses. |
| `rankText` | string | Global rank text including total. |
| `receivingFrom` | array<object> | Active Autonomous Systems sending traffic to this ASN. |
| `registeredCountry` | string | Registered country ISO code. |
| `registeredCountryName` | string | Localized registered country name. |
| `registrationLastChange` | string | Registration modification date. |
| `registry` | string | Regional Internet Registry the ASN is registered with. |
| `totalIpv4Addresses` | number | Total number of IPv4 addresses announced by the ASN. |
| `totalIpv4BogonPrefixes` | number | Total number of IPv4 bogon prefixes announced by the ASN. |
| `totalIpv4Prefixes` | number | Total number of IPv4 BGP prefixes announced by the ASN. |
| `totalIpv6BogonPrefixes` | number | Total number of IPv6 bogon prefixes announced by the ASN. |
| `totalIpv6Prefixes` | number | Total number of IPv6 BGP prefixes announced by the ASN. |
| `totalReceivingFrom` | number | Total number of active Autonomous Systems sending traffic to this ASN. |

## Native endpoint

Through the native BigDataCloud API, this operation is `GET /data/asn-info-receiving-from` (base URL `https://api-bdc.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-asn-receiving-from.md) for the provider-specific parameters and requirements.

