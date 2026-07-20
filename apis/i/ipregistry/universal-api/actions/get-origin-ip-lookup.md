# Ipregistry: Get Origin IP Lookup



```
GET https://connect.mindcloud.co/v1/universal/ipregistry/latest/actions/get-origin-ip-lookup
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ipregistry `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ipregistry/latest/actions/get-origin-ip-lookup?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ipregistry/latest/actions/get-origin-ip-lookup?${params}`, {
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

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `fields` | string | no | Optional response filter. Origin IP lookups also include user-agent data. Example: `location.country.name,connection.type`. |
| `hostname` | boolean | no | Set to true to include a fresh reverse DNS hostname lookup. |

## Response

```json
{
  "success": true,
  "data": [
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
      "type": "string",
      "user_agent": {
        "device": {
          "brand": "string",
          "name": "Ava Chen",
          "type": "string"
        },
        "engine": {
          "name": "Ava Chen",
          "type": "string",
          "version": "string",
          "version_major": "string"
        },
        "header": "string",
        "name": "Ava Chen",
        "os": {
          "name": "Ava Chen",
          "type": "string"
        },
        "type": "string",
        "version": "string",
        "version_major": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `carrier` | object |  |
| `company` | object |  |
| `company.domain` | string |  |
| `company.name` | string |  |
| `company.type` | string |  |
| `connection` | object |  |
| `connection.asn` | number |  |
| `connection.domain` | string |  |
| `connection.organization` | string |  |
| `connection.route` | string |  |
| `connection.type` | string |  |
| `currency` | object |  |
| `currency.code` | string |  |
| `currency.format` | object |  |
| `currency.format.decimal_separator` | string |  |
| `currency.format.group_separator` | string |  |
| `currency.format.negative` | object |  |
| `currency.format.negative.prefix` | string |  |
| `currency.format.negative.suffix` | string |  |
| `currency.format.positive` | object |  |
| `currency.format.positive.prefix` | string |  |
| `currency.format.positive.suffix` | string |  |
| `currency.name` | string |  |
| `currency.name_native` | string |  |
| `currency.plural` | string |  |
| `currency.plural_native` | string |  |
| `currency.symbol` | string |  |
| `currency.symbol_native` | string |  |
| `ip` | string |  |
| `location` | object |  |
| `location.city` | string |  |
| `location.continent` | object |  |
| `location.continent.code` | string |  |
| `location.continent.name` | string |  |
| `location.country` | object |  |
| `location.country.area` | number |  |
| `location.country.borders` | array<string> |  |
| `location.country.borders[]` | string |  |
| `location.country.calling_code` | string |  |
| `location.country.capital` | string |  |
| `location.country.code` | string |  |
| `location.country.flag` | object |  |
| `location.country.flag.emoji` | string |  |
| `location.country.flag.emoji_unicode` | string |  |
| `location.country.flag.emojitwo` | string |  |
| `location.country.flag.noto` | string |  |
| `location.country.flag.twemoji` | string |  |
| `location.country.flag.wikimedia` | string |  |
| `location.country.languages` | array<object> |  |
| `location.country.languages[]` | object |  |
| `location.country.languages[].code` | string |  |
| `location.country.languages[].name` | string |  |
| `location.country.languages[].native` | string |  |
| `location.country.name` | string |  |
| `location.country.population` | number |  |
| `location.country.population_density` | number |  |
| `location.country.tld` | string |  |
| `location.in_eu` | boolean |  |
| `location.language` | object |  |
| `location.language.code` | string |  |
| `location.language.name` | string |  |
| `location.language.native` | string |  |
| `location.latitude` | number |  |
| `location.longitude` | number |  |
| `location.postal` | string |  |
| `location.region` | object |  |
| `location.region.code` | string |  |
| `location.region.name` | string |  |
| `security` | object |  |
| `security.is_abuser` | boolean |  |
| `security.is_anonymous` | boolean |  |
| `security.is_attacker` | boolean |  |
| `security.is_bogon` | boolean |  |
| `security.is_cloud_provider` | boolean |  |
| `security.is_proxy` | boolean |  |
| `security.is_relay` | boolean |  |
| `security.is_threat` | boolean |  |
| `security.is_tor` | boolean |  |
| `security.is_tor_exit` | boolean |  |
| `security.is_vpn` | boolean |  |
| `time_zone` | object |  |
| `time_zone.abbreviation` | string |  |
| `time_zone.current_time` | string |  |
| `time_zone.id` | string |  |
| `time_zone.in_daylight_saving` | boolean |  |
| `time_zone.name` | string |  |
| `time_zone.offset` | number |  |
| `type` | string |  |
| `user_agent` | object |  |
| `user_agent.device` | object |  |
| `user_agent.device.brand` | string |  |
| `user_agent.device.name` | string |  |
| `user_agent.device.type` | string |  |
| `user_agent.engine` | object |  |
| `user_agent.engine.name` | string |  |
| `user_agent.engine.type` | string |  |
| `user_agent.engine.version` | string |  |
| `user_agent.engine.version_major` | string |  |
| `user_agent.header` | string |  |
| `user_agent.name` | string |  |
| `user_agent.os` | object |  |
| `user_agent.os.name` | string |  |
| `user_agent.os.type` | string |  |
| `user_agent.type` | string |  |
| `user_agent.version` | string |  |
| `user_agent.version_major` | string |  |

## Native endpoint

Through the native Ipregistry API, this operation is `GET /` (base URL `https://api.ipregistry.co`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-origin-ip-lookup.md) for the provider-specific parameters and requirements.

