# Precisely: Key Lookup

Retrieves an address from Precisely by PreciselyID or EIR code.

```
GET https://connect.mindcloud.co/v1/universal/precisely/latest/actions/key-lookup
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Precisely `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/precisely/latest/actions/key-lookup?connectionId=$CONNECTION_ID&key=string&type=PB_KEY" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "key": "string",
  "type": "PB_KEY"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/precisely/latest/actions/key-lookup?${params}`, {
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
| `key` | string | yes | Precisely geocode key value to look up. |
| `type` | string | yes | Key type, for example PB_KEY. Default: `PB_KEY`. |
| `country` | string | no | ISO country code or country name. |
| `objectId` | number | no | Optional object identifier for the lookup request. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "address": {
        "addressLastLine": "string",
        "addressNumber": "string",
        "areaName1": "Ava Chen",
        "areaName2": "Ava Chen",
        "areaName3": "Ava Chen",
        "country": "string",
        "customFields": {
          "PB_KEY": "string"
        },
        "mainAddressLine": "string",
        "postCode1": "string",
        "postCode2": "string",
        "streetName": "Ava Chen"
      },
      "formattedLocationAddress": "string",
      "formattedStreetAddress": "string",
      "geometry": {
        "coordinates": [
          1
        ],
        "type": "string"
      },
      "identifier": "string",
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
| `address.addressLastLine` | string | City, region, and postal line. |
| `address.addressNumber` | string | Address number. |
| `address.areaName1` | string | Top-level administrative area, typically state or province. |
| `address.areaName2` | string | Secondary administrative area, typically county or district. |
| `address.areaName3` | string | City or locality name. |
| `address.country` | string | Country code or country name. |
| `address.customFields.PB_KEY` | string | Precisely PB key for the matched location. |
| `address.mainAddressLine` | string | Primary street-address line. |
| `address.postCode1` | string | Primary postal code. |
| `address.postCode2` | string | Postal code extension. |
| `address.streetName` | string | Street name. |
| `formattedLocationAddress` | string | Formatted city, region, and postal line. |
| `formattedStreetAddress` | string | Formatted street-address line. |
| `geometry.coordinates` | array<number> | Longitude and latitude coordinates. |
| `geometry.type` | string | GeoJSON geometry type. |
| `identifier` | string | Provider-specific identifier for the matched location. |
| `precisionCode` | string | Precisely precision code for the match. |
| `precisionLevel` | number | Matched precision level returned for the candidate. |
| `ranges` | array<object> | Range metadata returned for the candidate. |
| `sourceDictionary` | string | Precisely source dictionary identifier. |

## Native endpoint

Through the native Precisely API, this operation is `GET /geocode/v1/keylookup` (base URL `https://api.precisely.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/key-lookup.md) for the provider-specific parameters and requirements.

