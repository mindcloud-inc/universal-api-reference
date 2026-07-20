# Ipregistry: Get Batch ASN Lookup



```
GET https://connect.mindcloud.co/v1/universal/ipregistry/latest/actions/get-batch-asn-lookup
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ipregistry `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ipregistry/latest/actions/get-batch-asn-lookup?connectionId=$CONNECTION_ID&asns=AS15169%2CAS13335" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "asns": "AS15169,AS13335"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ipregistry/latest/actions/get-batch-asn-lookup?${params}`, {
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
| `asns` | string | yes | Comma-separated list of up to 16 Autonomous System Numbers. Example: `AS15169,AS13335`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `fields` | string | no | Optional response filter applied to each ASN result item. Example: `name,type`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "results": [
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
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `results` | array<object> |  |
| `results[]` | object |  |
| `results[].allocated` | string |  |
| `results[].asn` | number |  |
| `results[].country_code` | string |  |
| `results[].domain` | string |  |
| `results[].name` | string |  |
| `results[].prefixes` | object |  |
| `results[].prefixes.ipv4` | array<object> |  |
| `results[].prefixes.ipv4_count` | number |  |
| `results[].prefixes.ipv4[]` | object |  |
| `results[].prefixes.ipv4[].cidr` | string |  |
| `results[].prefixes.ipv4[].country_code` | string |  |
| `results[].prefixes.ipv4[].network_name` | string |  |
| `results[].prefixes.ipv4[].organization` | string |  |
| `results[].prefixes.ipv4[].registry` | string |  |
| `results[].prefixes.ipv4[].size` | number |  |
| `results[].prefixes.ipv4[].status` | string |  |
| `results[].prefixes.ipv6` | array<object> |  |
| `results[].prefixes.ipv6_count` | number |  |
| `results[].prefixes.ipv6[]` | object |  |
| `results[].prefixes.ipv6[].cidr` | string |  |
| `results[].prefixes.ipv6[].country_code` | string |  |
| `results[].prefixes.ipv6[].network_name` | string |  |
| `results[].prefixes.ipv6[].organization` | string |  |
| `results[].prefixes.ipv6[].registry` | string |  |
| `results[].prefixes.ipv6[].size` | number |  |
| `results[].prefixes.ipv6[].status` | string |  |
| `results[].registry` | string |  |
| `results[].relationships` | object |  |
| `results[].relationships.downstreams` | array<number> |  |
| `results[].relationships.downstreams[]` | number |  |
| `results[].relationships.peers` | array<number> |  |
| `results[].relationships.peers[]` | number |  |
| `results[].relationships.upstreams` | array<number> |  |
| `results[].relationships.upstreams[]` | number |  |
| `results[].type` | string |  |
| `results[].updated` | string |  |

## Native endpoint

Through the native Ipregistry API, this operation is `GET /:asns` (base URL `https://api.ipregistry.co`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-batch-asn-lookup.md) for the provider-specific parameters and requirements.

