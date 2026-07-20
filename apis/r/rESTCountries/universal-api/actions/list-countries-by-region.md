# REST Countries: List Countries by Region



```
GET https://connect.mindcloud.co/v1/universal/rESTCountries/latest/actions/list-countries-by-region
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a REST Countries `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rESTCountries/latest/actions/list-countries-by-region?connectionId=$CONNECTION_ID&region=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "region": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rESTCountries/latest/actions/list-countries-by-region?${params}`, {
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
| `region` | string | yes | Region such as Europe or Africa. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "altSpellings": [
        "string"
      ],
      "area": 1,
      "borders": [
        "string"
      ],
      "capital": [
        "string"
      ],
      "capitalInfo": {
        "latlng": [
          1
        ]
      },
      "car": {
        "side": "string",
        "signs": [
          "string"
        ]
      },
      "cca2": "string",
      "cca3": "string",
      "ccn3": "string",
      "cioc": "string",
      "coatOfArms": {
        "png": "string",
        "svg": "string"
      },
      "continents": [
        "string"
      ],
      "currencies": {},
      "demonyms": {},
      "fifa": "string",
      "flag": "string",
      "flags": {
        "alt": "string",
        "png": "string",
        "svg": "string"
      },
      "idd": {
        "root": "string",
        "suffixes": [
          "string"
        ]
      },
      "independent": true,
      "landlocked": true,
      "languages": {},
      "latlng": [
        1
      ],
      "maps": {
        "googleMaps": "string",
        "openStreetMaps": "string"
      },
      "name": {
        "common": "Ava Chen",
        "nativeName": {},
        "official": "Ava Chen"
      },
      "population": 1,
      "postalCode": {
        "format": "string",
        "regex": "string"
      },
      "region": "string",
      "startOfWeek": "string",
      "status": "string",
      "subregion": "string",
      "timezones": [
        "string"
      ],
      "tld": [
        "string"
      ],
      "translations": {},
      "unMember": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `altSpellings` | array<string> |  |
| `area` | number |  |
| `borders` | array<string> |  |
| `capital` | array<string> |  |
| `capitalInfo.latlng` | array<number> |  |
| `car.side` | string |  |
| `car.signs` | array<string> |  |
| `cca2` | string |  |
| `cca3` | string |  |
| `ccn3` | string |  |
| `cioc` | string |  |
| `coatOfArms.png` | string |  |
| `coatOfArms.svg` | string |  |
| `continents` | array<string> |  |
| `currencies` | object |  |
| `demonyms` | object |  |
| `fifa` | string |  |
| `flag` | string |  |
| `flags.alt` | string |  |
| `flags.png` | string |  |
| `flags.svg` | string |  |
| `idd.root` | string |  |
| `idd.suffixes` | array<string> |  |
| `independent` | boolean |  |
| `landlocked` | boolean |  |
| `languages` | object |  |
| `latlng` | array<number> |  |
| `maps.googleMaps` | string |  |
| `maps.openStreetMaps` | string |  |
| `name.common` | string |  |
| `name.nativeName` | object |  |
| `name.official` | string |  |
| `population` | number |  |
| `postalCode.format` | string |  |
| `postalCode.regex` | string |  |
| `region` | string |  |
| `startOfWeek` | string |  |
| `status` | string |  |
| `subregion` | string |  |
| `timezones` | array<string> |  |
| `tld` | array<string> |  |
| `translations` | object |  |
| `unMember` | boolean |  |

## Native endpoint

Through the native REST Countries API, this operation is `GET region/:region` (base URL `https://restcountries.com/v3.1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-countries-by-region.md) for the provider-specific parameters and requirements.

