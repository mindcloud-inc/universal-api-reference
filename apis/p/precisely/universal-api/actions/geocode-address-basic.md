# Precisely: Geocode Address (Basic)

Retrieves geocoding candidates from Precisely for an address.

```
GET https://connect.mindcloud.co/v1/universal/precisely/latest/actions/geocode-address-basic
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Precisely `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/precisely/latest/actions/geocode-address-basic?connectionId=$CONNECTION_ID&mainAddress=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "mainAddress": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/precisely/latest/actions/geocode-address-basic?${params}`, {
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
| `mainAddress` | string | yes | Single-line input address, or the street-address portion when structured fields are used. |
| `placeName` | string | no | Building, place, point of interest, company, or firm name associated with the address. |
| `lastLine` | string | no | The last line of the address. |
| `areaName1` | string | no | Largest geographic area, typically a state or province. |
| `areaName3` | string | no | City or town name. |
| `postalCode` | string | no | Postal code in the appropriate format for the selected country. |
| `country` | string | no | ISO country code or country name. |
| `matchMode` | string | no | Controls how strictly the address is matched. |
| `maxCands` | number | no | Maximum number of candidates to return. |
| `removeAccentMarks` | boolean | no | Suppress accents and diacritical marks in the output. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "address": {
        "addressLastLine": "string",
        "areaName1": "Ava Chen",
        "areaName2": "Ava Chen",
        "areaName3": "Ava Chen",
        "country": "string",
        "customFields": {
          "ADDRESS_LINE1": "string"
        }
      },
      "formattedLocationAddress": "string",
      "geometry": {
        "coordinates": [
          1
        ],
        "type": "string"
      },
      "precisionCode": "string",
      "precisionLevel": 1,
      "ranges": [
        {}
      ],
      "sourceDictionary": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address.addressLastLine` | string | City, county, region, and country line. |
| `address.areaName1` | string | Top-level administrative area, typically state or province. |
| `address.areaName2` | string | Secondary administrative area, typically county or district. |
| `address.areaName3` | string | City or locality name. |
| `address.country` | string | Country code or country name. |
| `address.customFields.ADDRESS_LINE1` | string | Provider-specific primary address line metadata. |
| `formattedLocationAddress` | string | Formatted geocoded address string. |
| `geometry.coordinates` | array<number> | Longitude and latitude coordinates. |
| `geometry.type` | string | GeoJSON geometry type. |
| `precisionCode` | string | Precisely precision code for the match. |
| `precisionLevel` | number | Matched precision level returned for the candidate. |
| `ranges` | array<object> | Range metadata returned for the candidate. |
| `sourceDictionary` | string | Precisely source dictionary identifier. |

## Native endpoint

Through the native Precisely API, this operation is `GET /geocode/v1/basic/geocode` (base URL `https://api.precisely.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/geocode-address-basic.md) for the provider-specific parameters and requirements.

