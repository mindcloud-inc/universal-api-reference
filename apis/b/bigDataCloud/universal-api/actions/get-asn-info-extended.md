# BigDataCloud: Get ASN Info Extended

Retrieves extended ASN details from BigDataCloud.

```
GET https://connect.mindcloud.co/v1/universal/bigDataCloud/latest/actions/get-asn-info-extended
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BigDataCloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bigDataCloud/latest/actions/get-asn-info-extended?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bigDataCloud/latest/actions/get-asn-info-extended?${params}`, {
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
| `asn` | string | no | Autonomous System Number as numeric or ASN format, for example 123, AS123, or ASN123. Example: `AS14618`. |
| `localityLanguage` | string | no | Preferred language for localized place and country names. Default: `en`. Example: `en`. |
| `peersCap` | number | no | Maximum number of receivingFrom and transitTo entries to retrieve. Default and hard limit are 50. Example: `50`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "asn": "string",
      "asnNumeric": 1,
      "confidenceArea": [
        {}
      ],
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
      "totalReceivingFrom": 1,
      "totalTransitTo": 1,
      "transitTo": [
        {}
      ]
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
| `confidenceArea` | array<object> | Most active geographical area detected for the ASN. |
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
| `totalTransitTo` | number | Total number of active Autonomous Systems receiving traffic from this ASN. |
| `transitTo` | array<object> | Active Autonomous Systems receiving traffic from this ASN. |

## Native endpoint

Through the native BigDataCloud API, this operation is `GET /data/asn-info-full` (base URL `https://api-bdc.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-asn-info-extended.md) for the provider-specific parameters and requirements.

