# Ipregistry: Get ASN Lookup



```
GET https://connect.mindcloud.co/v1/universal/ipregistry/latest/actions/get-asn-lookup
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ipregistry `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ipregistry/latest/actions/get-asn-lookup?connectionId=$CONNECTION_ID&asn=AS15169" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "asn": "AS15169"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ipregistry/latest/actions/get-asn-lookup?${params}`, {
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
| `asn` | string | yes | Autonomous System Number to look up, for example `AS15169`. Example: `AS15169`. |
| `fields` | string | no | Optional response filter for ASN lookup results. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "allocated": "string",
      "asn": 1,
      "country_code": "string",
      "domain": "string",
      "name": "Ava Chen",
      "prefixes": {
        "ipv4": [
          {
            "cidr": "string",
            "country_code": "string",
            "network_name": "Ava Chen",
            "organization": "string",
            "registry": "string",
            "size": 1,
            "status": "string"
          }
        ],
        "ipv4_count": 1,
        "ipv6": [
          {
            "cidr": "string",
            "country_code": "string",
            "network_name": "Ava Chen",
            "organization": "string",
            "registry": "string",
            "size": 1,
            "status": "string"
          }
        ],
        "ipv6_count": 1
      },
      "registry": "string",
      "relationships": {
        "downstreams": [
          1
        ],
        "peers": [
          1
        ],
        "upstreams": [
          1
        ]
      },
      "type": "string",
      "updated": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `allocated` | string |  |
| `asn` | number |  |
| `country_code` | string |  |
| `domain` | string |  |
| `name` | string |  |
| `prefixes` | object |  |
| `prefixes.ipv4` | array<object> |  |
| `prefixes.ipv4_count` | number |  |
| `prefixes.ipv4[]` | object |  |
| `prefixes.ipv4[].cidr` | string |  |
| `prefixes.ipv4[].country_code` | string |  |
| `prefixes.ipv4[].network_name` | string |  |
| `prefixes.ipv4[].organization` | string |  |
| `prefixes.ipv4[].registry` | string |  |
| `prefixes.ipv4[].size` | number |  |
| `prefixes.ipv4[].status` | string |  |
| `prefixes.ipv6` | array<object> |  |
| `prefixes.ipv6_count` | number |  |
| `prefixes.ipv6[]` | object |  |
| `prefixes.ipv6[].cidr` | string |  |
| `prefixes.ipv6[].country_code` | string |  |
| `prefixes.ipv6[].network_name` | string |  |
| `prefixes.ipv6[].organization` | string |  |
| `prefixes.ipv6[].registry` | string |  |
| `prefixes.ipv6[].size` | number |  |
| `prefixes.ipv6[].status` | string |  |
| `registry` | string |  |
| `relationships` | object |  |
| `relationships.downstreams` | array<number> |  |
| `relationships.downstreams[]` | number |  |
| `relationships.peers` | array<number> |  |
| `relationships.peers[]` | number |  |
| `relationships.upstreams` | array<number> |  |
| `relationships.upstreams[]` | number |  |
| `type` | string |  |
| `updated` | string |  |

## Native endpoint

Through the native Ipregistry API, this operation is `GET /:asn` (base URL `https://api.ipregistry.co`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-asn-lookup.md) for the provider-specific parameters and requirements.

