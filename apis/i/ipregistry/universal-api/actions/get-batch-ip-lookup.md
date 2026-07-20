# Ipregistry: Get Batch IP Lookup



```
GET https://connect.mindcloud.co/v1/universal/ipregistry/latest/actions/get-batch-ip-lookup
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ipregistry `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ipregistry/latest/actions/get-batch-ip-lookup?connectionId=$CONNECTION_ID&ipAddresses=8.8.8.8%2C1.1.1.1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "ipAddresses": "8.8.8.8,1.1.1.1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ipregistry/latest/actions/get-batch-ip-lookup?${params}`, {
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
| `ipAddresses` | string | yes | Comma-separated list of up to 1024 IPv4 or IPv6 addresses. Example: `8.8.8.8,1.1.1.1`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `fields` | string | no | Optional response filter applied to each result item. Example: `location.country.code,location.country.name`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "results": [
        {
          "carrier": {},
          "company": {
            "domain": "string",
            "name": "Ava Chen",
            "type": "string"
          },
          "connection": {
            "asn": 1,
            "domain": "string",
            "organization": "string",
            "route": "string",
            "type": "string"
          },
          "currency": {
            "code": "string",
            "format": {
              "decimal_separator": "string",
              "group_separator": "string",
              "negative": {
                "prefix": "string",
                "suffix": "string"
              },
              "positive": {
                "prefix": "string",
                "suffix": "string"
              }
            },
            "name": "Ava Chen",
            "name_native": "Ava Chen",
            "plural": "string",
            "plural_native": "string",
            "symbol": "string",
            "symbol_native": "string"
          },
          "ip": "string",
          "location": {
            "city": "string",
            "continent": {
              "code": "string",
              "name": "Ava Chen"
            },
            "country": {
              "area": 1,
              "borders": [
                "string"
              ],
              "calling_code": "string",
              "capital": "string",
              "code": "string",
              "flag": {
                "emoji": "string",
                "emoji_unicode": "string",
                "emojitwo": "string",
                "noto": "string",
                "twemoji": "string",
                "wikimedia": "string"
              },
              "languages": [
                {
                  "code": "string",
                  "name": "Ava Chen",
                  "native": "string"
                }
              ],
              "name": "Ava Chen",
              "population": 1,
              "population_density": 1,
              "tld": "string"
            },
            "in_eu": true,
            "language": {
              "code": "string",
              "name": "Ava Chen",
              "native": "string"
            },
            "latitude": 1,
            "longitude": 1,
            "postal": "string",
            "region": {
              "code": "string",
              "name": "Ava Chen"
            }
          },
          "security": {
            "is_abuser": true,
            "is_anonymous": true,
            "is_attacker": true,
            "is_bogon": true,
            "is_cloud_provider": true,
            "is_proxy": true,
            "is_relay": true,
            "is_threat": true,
            "is_tor": true,
            "is_tor_exit": true,
            "is_vpn": true
          },
          "time_zone": {
            "abbreviation": "string",
            "current_time": "string",
            "id": "string",
            "in_daylight_saving": true,
            "name": "Ava Chen",
            "offset": 1
          },
          "type": "string"
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
| `results[].carrier` | object |  |
| `results[].company` | object |  |
| `results[].company.domain` | string |  |
| `results[].company.name` | string |  |
| `results[].company.type` | string |  |
| `results[].connection` | object |  |
| `results[].connection.asn` | number |  |
| `results[].connection.domain` | string |  |
| `results[].connection.organization` | string |  |
| `results[].connection.route` | string |  |
| `results[].connection.type` | string |  |
| `results[].currency` | object |  |
| `results[].currency.code` | string |  |
| `results[].currency.format` | object |  |
| `results[].currency.format.decimal_separator` | string |  |
| `results[].currency.format.group_separator` | string |  |
| `results[].currency.format.negative` | object |  |
| `results[].currency.format.negative.prefix` | string |  |
| `results[].currency.format.negative.suffix` | string |  |
| `results[].currency.format.positive` | object |  |
| `results[].currency.format.positive.prefix` | string |  |
| `results[].currency.format.positive.suffix` | string |  |
| `results[].currency.name` | string |  |
| `results[].currency.name_native` | string |  |
| `results[].currency.plural` | string |  |
| `results[].currency.plural_native` | string |  |
| `results[].currency.symbol` | string |  |
| `results[].currency.symbol_native` | string |  |
| `results[].ip` | string |  |
| `results[].location` | object |  |
| `results[].location.city` | string |  |
| `results[].location.continent` | object |  |
| `results[].location.continent.code` | string |  |
| `results[].location.continent.name` | string |  |
| `results[].location.country` | object |  |
| `results[].location.country.area` | number |  |
| `results[].location.country.borders` | array<string> |  |
| `results[].location.country.borders[]` | string |  |
| `results[].location.country.calling_code` | string |  |
| `results[].location.country.capital` | string |  |
| `results[].location.country.code` | string |  |
| `results[].location.country.flag` | object |  |
| `results[].location.country.flag.emoji` | string |  |
| `results[].location.country.flag.emoji_unicode` | string |  |
| `results[].location.country.flag.emojitwo` | string |  |
| `results[].location.country.flag.noto` | string |  |
| `results[].location.country.flag.twemoji` | string |  |
| `results[].location.country.flag.wikimedia` | string |  |
| `results[].location.country.languages` | array<object> |  |
| `results[].location.country.languages[]` | object |  |
| `results[].location.country.languages[].code` | string |  |
| `results[].location.country.languages[].name` | string |  |
| `results[].location.country.languages[].native` | string |  |
| `results[].location.country.name` | string |  |
| `results[].location.country.population` | number |  |
| `results[].location.country.population_density` | number |  |
| `results[].location.country.tld` | string |  |
| `results[].location.in_eu` | boolean |  |
| `results[].location.language` | object |  |
| `results[].location.language.code` | string |  |
| `results[].location.language.name` | string |  |
| `results[].location.language.native` | string |  |
| `results[].location.latitude` | number |  |
| `results[].location.longitude` | number |  |
| `results[].location.postal` | string |  |
| `results[].location.region` | object |  |
| `results[].location.region.code` | string |  |
| `results[].location.region.name` | string |  |
| `results[].security` | object |  |
| `results[].security.is_abuser` | boolean |  |
| `results[].security.is_anonymous` | boolean |  |
| `results[].security.is_attacker` | boolean |  |
| `results[].security.is_bogon` | boolean |  |
| `results[].security.is_cloud_provider` | boolean |  |
| `results[].security.is_proxy` | boolean |  |
| `results[].security.is_relay` | boolean |  |
| `results[].security.is_threat` | boolean |  |
| `results[].security.is_tor` | boolean |  |
| `results[].security.is_tor_exit` | boolean |  |
| `results[].security.is_vpn` | boolean |  |
| `results[].time_zone` | object |  |
| `results[].time_zone.abbreviation` | string |  |
| `results[].time_zone.current_time` | string |  |
| `results[].time_zone.id` | string |  |
| `results[].time_zone.in_daylight_saving` | boolean |  |
| `results[].time_zone.name` | string |  |
| `results[].time_zone.offset` | number |  |
| `results[].type` | string |  |

## Native endpoint

Through the native Ipregistry API, this operation is `GET /:ipAddresses` (base URL `https://api.ipregistry.co`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-batch-ip-lookup.md) for the provider-specific parameters and requirements.

