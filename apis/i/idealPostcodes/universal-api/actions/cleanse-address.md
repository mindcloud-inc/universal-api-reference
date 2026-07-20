# Ideal Postcodes: Cleanse Address

Finds the closest matching address in Ideal Postcodes.

```
GET https://connect.mindcloud.co/v1/universal/idealPostcodes/latest/actions/cleanse-address
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ideal Postcodes `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/idealPostcodes/latest/actions/cleanse-address?connectionId=$CONNECTION_ID&query=10%20Downing%20Street%2C%20London%2C%20SW1A%202BN" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "10 Downing Street, London, SW1A 2BN"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/idealPostcodes/latest/actions/cleanse-address?${params}`, {
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
| `query` | string | yes | Freeform address input to cleanse. Default: `10 Downing Street, London, SW1A 2BN`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `postcode` | string | no | Optional postcode for the address. |
| `postTown` | string | no | Optional town or city component for the address. |
| `county` | string | no | Optional county or state component for the address. |
| `context` | string | no | Country context to use when cleansing the address, for example GBR. |
| `tags` | string | no | Comma-separated tags used to annotate the request context. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "confidence": 1,
      "count": 1,
      "fit": 1,
      "localityMatch": "string",
      "match": {
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
      },
      "organisationMatch": "string",
      "postcodeMatch": "string",
      "postTownMatch": "string",
      "premiseMatch": "string",
      "query": "string",
      "thoroughfareMatch": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `confidence` | number |  |
| `count` | number |  |
| `fit` | number |  |
| `localityMatch` | string |  |
| `match.administrativeCounty` | string |  |
| `match.buildingName` | string |  |
| `match.buildingNumber` | string |  |
| `match.country` | string |  |
| `match.countryIso` | string |  |
| `match.countryIso2` | string |  |
| `match.county` | string |  |
| `match.countyCode` | string |  |
| `match.dataset` | string |  |
| `match.deliveryPointSuffix` | string |  |
| `match.departmentName` | string |  |
| `match.dependantLocality` | string |  |
| `match.dependantThoroughfare` | string |  |
| `match.district` | string |  |
| `match.doubleDependantLocality` | string |  |
| `match.eastings` | number |  |
| `match.id` | string |  |
| `match.language` | string |  |
| `match.latitude` | number |  |
| `match.line1` | string |  |
| `match.line2` | string |  |
| `match.line3` | string |  |
| `match.longitude` | number |  |
| `match.northings` | number |  |
| `match.organisationName` | string |  |
| `match.poBox` | string |  |
| `match.postalCounty` | string |  |
| `match.postcode` | string |  |
| `match.postcodeInward` | string |  |
| `match.postcodeOutward` | string |  |
| `match.postcodeType` | string |  |
| `match.postTown` | string |  |
| `match.premise` | string |  |
| `match.subBuildingName` | string |  |
| `match.suOrganisationIndicator` | string |  |
| `match.thoroughfare` | string |  |
| `match.traditionalCounty` | string |  |
| `match.udprn` | number |  |
| `match.umprn` | string |  |
| `match.uprn` | string |  |
| `match.ward` | string |  |
| `organisationMatch` | string |  |
| `postcodeMatch` | string |  |
| `postTownMatch` | string |  |
| `premiseMatch` | string |  |
| `query` | string |  |
| `thoroughfareMatch` | string |  |

## Native endpoint

Through the native Ideal Postcodes API, this operation is `POST /cleanse/addresses` (base URL `https://api.ideal-postcodes.co.uk/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/cleanse-address.md) for the provider-specific parameters and requirements.

