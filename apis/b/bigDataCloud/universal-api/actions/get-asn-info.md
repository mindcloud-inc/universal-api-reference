# BigDataCloud: Get ASN Info

Retrieves ASN details from BigDataCloud.

```
GET https://connect.mindcloud.co/v1/universal/bigDataCloud/latest/actions/get-asn-info
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BigDataCloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bigDataCloud/latest/actions/get-asn-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bigDataCloud/latest/actions/get-asn-info?${params}`, {
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
| `asn` | string | no | Autonomous system number in numeric, AS, or ASN format. Example: `AS14618`. |
| `localityLanguage` | string | no | Preferred language for locality names in ISO 639-1 format. Default: `en`. Example: `en`. |

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
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `asn` | string |  |
| `asnNumeric` | number |  |
| `name` | string |  |
| `organisation` | string |  |
| `rank` | number |  |
| `rankText` | string |  |
| `registeredCountry` | string |  |
| `registeredCountryName` | string |  |
| `registrationLastChange` | date |  |
| `registry` | string |  |
| `totalIpv4Addresses` | number |  |
| `totalIpv4BogonPrefixes` | number |  |
| `totalIpv4Prefixes` | number |  |
| `totalIpv6BogonPrefixes` | number |  |
| `totalIpv6Prefixes` | number |  |

## Native endpoint

Through the native BigDataCloud API, this operation is `GET /data/asn-info` (base URL `https://api-bdc.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-asn-info.md) for the provider-specific parameters and requirements.

