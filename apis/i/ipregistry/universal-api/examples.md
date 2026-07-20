# Ipregistry Universal API Examples

These examples use the MindCloud API key and Ipregistry connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Origin IP Lookup



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

Example response:

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

See the full [Get Origin IP Lookup action reference](actions/get-origin-ip-lookup.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/ipregistry/latest/actions/get-origin-ip-lookup).
