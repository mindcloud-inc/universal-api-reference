# Ideal Postcodes: Find Address

Finds address suggestions in Ideal Postcodes by text query.

```
GET https://connect.mindcloud.co/v1/universal/idealPostcodes/latest/actions/find-address
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ideal Postcodes `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/idealPostcodes/latest/actions/find-address?connectionId=$CONNECTION_ID&query=10%20downing" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "10 downing"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/idealPostcodes/latest/actions/find-address?${params}`, {
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
| `query` | string | yes | Partial address string to autocomplete. Default: `10 downing`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `dataset` | string | no | Comma-separated datasets to search within. |
| `context` | string | no | Context to limit results, typically a country code. |
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
| `biasIp` | boolean | no | Set to true to bias results using the request IP location. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "suggestion": "string",
      "udprn": 1,
      "urls": {
        "udprn": "https://example.com"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `suggestion` | string |  |
| `udprn` | number |  |
| `urls.udprn` | string |  |

## Native endpoint

Through the native Ideal Postcodes API, this operation is `GET /autocomplete/addresses` (base URL `https://api.ideal-postcodes.co.uk/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/find-address.md) for the provider-specific parameters and requirements.

