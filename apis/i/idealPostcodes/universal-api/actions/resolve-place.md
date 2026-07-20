# Ideal Postcodes: Resolve Place

Retrieves a place from Ideal Postcodes by place ID.

```
GET https://connect.mindcloud.co/v1/universal/idealPostcodes/latest/actions/resolve-place
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ideal Postcodes `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/idealPostcodes/latest/actions/resolve-place?connectionId=$CONNECTION_ID&place=geonames_2643743" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "place": "geonames_2643743"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/idealPostcodes/latest/actions/resolve-place?${params}`, {
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
| `place` | string | yes | Place suggestion ID to resolve. Default: `geonames_2643743`. |

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
      "countryIso": "string",
      "dataset": "string",
      "descriptiveName": "Ava Chen",
      "id": "string",
      "language": "string",
      "latitude": 1,
      "longitude": 1,
      "name": "Ava Chen",
      "native": {
        "admin1Code": "string",
        "admin1Geonameid": 1,
        "admin1Name": "Ava Chen",
        "admin2Code": "string",
        "admin2Geonameid": 1,
        "admin2Name": "Ava Chen",
        "admin3Code": "string",
        "admin4Code": "string",
        "alternatenames": [
          "Ava Chen"
        ],
        "asciiname": "Ava Chen",
        "cc2": [
          "string"
        ],
        "countryCode": "string",
        "countryIso": "string",
        "dataset": "string",
        "dem": 1,
        "elevation": 1,
        "featureClass": "string",
        "featureCode": "string",
        "geonameid": 1,
        "id": "string",
        "language": "string",
        "latitude": 1,
        "longitude": 1,
        "modificationDate": "2026-05-07T12:00:00.000Z",
        "name": "Ava Chen",
        "population": "string",
        "timezone": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `countryIso` | string |  |
| `dataset` | string |  |
| `descriptiveName` | string |  |
| `id` | string |  |
| `language` | string |  |
| `latitude` | number |  |
| `longitude` | number |  |
| `name` | string |  |
| `native.admin1Code` | string |  |
| `native.admin1Geonameid` | number |  |
| `native.admin1Name` | string |  |
| `native.admin2Code` | string |  |
| `native.admin2Geonameid` | number |  |
| `native.admin2Name` | string |  |
| `native.admin3Code` | string |  |
| `native.admin4Code` | string |  |
| `native.alternatenames[]` | string |  |
| `native.asciiname` | string |  |
| `native.cc2[]` | string |  |
| `native.countryCode` | string |  |
| `native.countryIso` | string |  |
| `native.dataset` | string |  |
| `native.dem` | number |  |
| `native.elevation` | number |  |
| `native.featureClass` | string |  |
| `native.featureCode` | string |  |
| `native.geonameid` | number |  |
| `native.id` | string |  |
| `native.language` | string |  |
| `native.latitude` | number |  |
| `native.longitude` | number |  |
| `native.modificationDate` | date |  |
| `native.name` | string |  |
| `native.population` | string |  |
| `native.timezone` | string |  |

## Native endpoint

Through the native Ideal Postcodes API, this operation is `GET /places/:place` (base URL `https://api.ideal-postcodes.co.uk/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/resolve-place.md) for the provider-specific parameters and requirements.

