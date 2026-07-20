# Geoapify Geocode: IP Geolocation

Retrieves IP geolocation data from Geoapify.

```
GET https://connect.mindcloud.co/v1/universal/geoapify/latest/actions/ip-geolocation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Geoapify Geocode `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/geoapify/latest/actions/ip-geolocation?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/geoapify/latest/actions/ip-geolocation?${params}`, {
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
| `ip` | string | no | IPv4 or IPv6 address. If omitted, Geoapify uses the caller IP. Example: `8.8.8.8`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "city": {
        "name": "Ava Chen",
        "names": {
          "en": "Ava Chen"
        }
      },
      "continent": {
        "code": "string",
        "geonameId": 1,
        "name": "Ava Chen",
        "names": {
          "en": "Ava Chen"
        }
      },
      "country": {
        "capital": "string",
        "currency": "string",
        "flag": "string",
        "geonameId": 1,
        "isoCode": "string",
        "languages": [
          {
            "isoCode": "string",
            "name": "Ava Chen",
            "nameNative": "Ava Chen"
          }
        ],
        "name": "Ava Chen",
        "nameNative": "Ava Chen",
        "names": {
          "en": "Ava Chen"
        },
        "phoneCode": "string"
      },
      "datasource": [
        {
          "attribution": "string",
          "license": "string",
          "name": "Ava Chen"
        }
      ],
      "ip": "string",
      "location": {
        "latitude": 1,
        "longitude": 1
      },
      "state": {
        "name": "Ava Chen"
      },
      "subdivisions": [
        {
          "names": {
            "en": "Ava Chen"
          }
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
| `city.name` | string |  |
| `city.names.en` | string |  |
| `continent.code` | string |  |
| `continent.geonameId` | number |  |
| `continent.name` | string |  |
| `continent.names.en` | string |  |
| `country.capital` | string |  |
| `country.currency` | string |  |
| `country.flag` | string |  |
| `country.geonameId` | number |  |
| `country.isoCode` | string |  |
| `country.languages[].isoCode` | string |  |
| `country.languages[].name` | string |  |
| `country.languages[].nameNative` | string |  |
| `country.name` | string |  |
| `country.nameNative` | string |  |
| `country.names.en` | string |  |
| `country.phoneCode` | string |  |
| `datasource[].attribution` | string |  |
| `datasource[].license` | string |  |
| `datasource[].name` | string |  |
| `ip` | string |  |
| `location.latitude` | number |  |
| `location.longitude` | number |  |
| `state.name` | string |  |
| `subdivisions[].names.en` | string |  |

## Native endpoint

Through the native Geoapify Geocode API, this operation is `GET /ipinfo` (base URL `https://api.geoapify.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/ip-geolocation.md) for the provider-specific parameters and requirements.

