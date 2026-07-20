# Ideal Postcodes: Resolve Address

Retrieves a UK address from Ideal Postcodes by address ID.

```
GET https://connect.mindcloud.co/v1/universal/idealPostcodes/latest/actions/resolve-address
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ideal Postcodes `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/idealPostcodes/latest/actions/resolve-address?connectionId=$CONNECTION_ID&address=paf_23747771" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "address": "paf_23747771"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/idealPostcodes/latest/actions/resolve-address?${params}`, {
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
| `address` | string | yes | Address suggestion ID to resolve in UK format. Default: `paf_23747771`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `tags` | string | no | Comma-separated tags to associate with the resolution request. |

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

Through the native Ideal Postcodes API, this operation is `GET /autocomplete/addresses/:address/gbr` (base URL `https://api.ideal-postcodes.co.uk/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/resolve-address.md) for the provider-specific parameters and requirements.

