# Ideal Postcodes: Extract Addresses

Finds addresses in Ideal Postcodes by text query.

```
GET https://connect.mindcloud.co/v1/universal/idealPostcodes/latest/actions/extract-addresses
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ideal Postcodes `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/idealPostcodes/latest/actions/extract-addresses?connectionId=$CONNECTION_ID&limit=25&offset=0&query=10%20downing%20street%20london" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "query": "10 downing street london"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/idealPostcodes/latest/actions/extract-addresses?${params}`, {
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
| `query` | string | yes | Address text to query. Default: `10 downing street london`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `filter` | string | no | Comma-separated whitelist of response fields to return. |
| `lon` | number | no | Longitude for reverse geocoding; use together with latitude. |
| `lat` | number | no | Latitude for reverse geocoding; use together with longitude. |
| `postcodeOutward` | string | no | Filter results by outward postcode code. |
| `postcode` | string | no | Filter results by postcode. |
| `postcodeArea` | string | no | Filter results by postcode area. |
| `postcodeSector` | string | no | Filter results by postcode sector. |
| `postTown` | string | no | Filter results by town or city. |
| `uprn` | number | no | Filter results by UPRN. |
| `country` | string | no | Filter results by country name. |
| `postcodeType` | string | no | Filter results by postcode type. |
| `suOrganisationIndicator` | string | no | Filter results by organisation indicator. |
| `box` | string | no | Restrict search to a bounding box. |
| `biasPostcodeOutward` | string | no | Bias results toward a matching outward code. |
| `biasPostcode` | string | no | Bias results toward a matching postcode. |
| `biasPostcodeArea` | string | no | Bias results toward a matching postcode area. |
| `biasPostcodeSector` | string | no | Bias results toward a matching postcode sector. |
| `biasPostTown` | string | no | Bias results toward a matching town or city. |
| `biasThoroughfare` | string | no | Bias results toward a street or thoroughfare. |
| `biasCountry` | string | no | Bias results toward a matching country. |
| `biasLonlat` | string | no | Bias using longitude, latitude, and radius in meters. |
| `tags` | string | no | Comma-separated tags used to annotate the request context. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "administrativeCounty": "string",
      "buildingName": "Ava Chen",
      "buildingNumber": "string",
      "country": "string",
      "countryIso": "string",
      "countryIso2": "string",
      "county": "string",
      "countyCode": "string",
      "dataset": "string",
      "deliveryPointSuffix": "string",
      "departmentName": "Ava Chen",
      "dependantLocality": "string",
      "dependantThoroughfare": "string",
      "district": "string",
      "doubleDependantLocality": "string",
      "eastings": 1,
      "id": "string",
      "language": "string",
      "latitude": 1,
      "line1": "string",
      "line2": "string",
      "line3": "string",
      "longitude": 1,
      "northings": 1,
      "organisationName": "Ava Chen",
      "poBox": "string",
      "postalCounty": "string",
      "postcode": "string",
      "postcodeInward": "string",
      "postcodeOutward": "string",
      "postcodeType": "string",
      "postTown": "string",
      "premise": "string",
      "subBuildingName": "Ava Chen",
      "suOrganisationIndicator": "string",
      "thoroughfare": "string",
      "traditionalCounty": "string",
      "udprn": 1,
      "umprn": "string",
      "uprn": "string",
      "ward": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `administrativeCounty` | string |  |
| `buildingName` | string |  |
| `buildingNumber` | string |  |
| `country` | string |  |
| `countryIso` | string |  |
| `countryIso2` | string |  |
| `county` | string |  |
| `countyCode` | string |  |
| `dataset` | string |  |
| `deliveryPointSuffix` | string |  |
| `departmentName` | string |  |
| `dependantLocality` | string |  |
| `dependantThoroughfare` | string |  |
| `district` | string |  |
| `doubleDependantLocality` | string |  |
| `eastings` | number |  |
| `id` | string |  |
| `language` | string |  |
| `latitude` | number |  |
| `line1` | string |  |
| `line2` | string |  |
| `line3` | string |  |
| `longitude` | number |  |
| `northings` | number |  |
| `organisationName` | string |  |
| `poBox` | string |  |
| `postalCounty` | string |  |
| `postcode` | string |  |
| `postcodeInward` | string |  |
| `postcodeOutward` | string |  |
| `postcodeType` | string |  |
| `postTown` | string |  |
| `premise` | string |  |
| `subBuildingName` | string |  |
| `suOrganisationIndicator` | string |  |
| `thoroughfare` | string |  |
| `traditionalCounty` | string |  |
| `udprn` | number |  |
| `umprn` | string |  |
| `uprn` | string |  |
| `ward` | string |  |

## Native endpoint

Through the native Ideal Postcodes API, this operation is `GET /addresses` (base URL `https://api.ideal-postcodes.co.uk/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/extract-addresses.md) for the provider-specific parameters and requirements.

