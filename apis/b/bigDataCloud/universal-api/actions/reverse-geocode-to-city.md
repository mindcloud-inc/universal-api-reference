# BigDataCloud: Reverse Geocode to City

Reverse geocodes coordinates to a city in BigDataCloud.

```
GET https://connect.mindcloud.co/v1/universal/bigDataCloud/latest/actions/reverse-geocode-to-city
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BigDataCloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bigDataCloud/latest/actions/reverse-geocode-to-city?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bigDataCloud/latest/actions/reverse-geocode-to-city?${params}`, {
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
| `latitude` | number | no | Latitude value in the WGS 84 reference system. Example: `-34.93129`. |
| `longitude` | number | no | Longitude value in the WGS 84 reference system. Example: `138.59669`. |
| `localityLanguage` | string | no | Preferred language for locality names in ISO 639-1 format. Default: `en`. Example: `en`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "city": "string",
      "continent": "string",
      "continentCode": "string",
      "countryCode": "string",
      "countryName": "Ava Chen",
      "latitude": 1,
      "locality": "string",
      "localityInfo": {
        "administrative": [
          {
            "adminLevel": 1,
            "description": "string",
            "geonameId": 1,
            "isoCode": "string",
            "isoName": "Ava Chen",
            "name": "Ava Chen",
            "order": 1,
            "wikidataId": "string"
          }
        ],
        "informative": [
          {
            "description": "string",
            "geonameId": 1,
            "isoCode": "string",
            "isoName": "Ava Chen",
            "name": "Ava Chen",
            "order": 1,
            "wikidataId": "string"
          }
        ]
      },
      "localityLanguageRequested": "string",
      "longitude": 1,
      "plusCode": "string",
      "postcode": "string",
      "principalSubdivision": "string",
      "principalSubdivisionCode": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `city` | string |  |
| `continent` | string |  |
| `continentCode` | string |  |
| `countryCode` | string |  |
| `countryName` | string |  |
| `latitude` | number |  |
| `locality` | string |  |
| `localityInfo.administrative[].adminLevel` | number |  |
| `localityInfo.administrative[].description` | string |  |
| `localityInfo.administrative[].geonameId` | number |  |
| `localityInfo.administrative[].isoCode` | string |  |
| `localityInfo.administrative[].isoName` | string |  |
| `localityInfo.administrative[].name` | string |  |
| `localityInfo.administrative[].order` | number |  |
| `localityInfo.administrative[].wikidataId` | string |  |
| `localityInfo.informative[].description` | string |  |
| `localityInfo.informative[].geonameId` | number |  |
| `localityInfo.informative[].isoCode` | string |  |
| `localityInfo.informative[].isoName` | string |  |
| `localityInfo.informative[].name` | string |  |
| `localityInfo.informative[].order` | number |  |
| `localityInfo.informative[].wikidataId` | string |  |
| `localityLanguageRequested` | string |  |
| `longitude` | number |  |
| `plusCode` | string |  |
| `postcode` | string |  |
| `principalSubdivision` | string |  |
| `principalSubdivisionCode` | string |  |

## Native endpoint

Through the native BigDataCloud API, this operation is `GET /data/reverse-geocode` (base URL `https://api-bdc.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/reverse-geocode-to-city.md) for the provider-specific parameters and requirements.

