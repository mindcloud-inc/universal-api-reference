# Open Brewery DB: List Breweries

Retrieves breweries from Open Brewery DB.

```
GET https://connect.mindcloud.co/v1/universal/openBreweryDB/latest/actions/list-breweries
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Open Brewery DB `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/openBreweryDB/latest/actions/list-breweries?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/openBreweryDB/latest/actions/list-breweries?${params}`, {
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
| `byCity` | string | no | Filter breweries by city. Use underscores or URL encoding for spaces. |
| `byCountry` | string | no | Filter breweries by country. Use underscores or URL encoding for spaces. |
| `byName` | string | no | Filter breweries by name. Use underscores or URL encoding for spaces. |
| `byState` | string | no | Filter breweries by full state name; abbreviations are not supported. |
| `byType` | list | no | Filter by brewery type: micro, nano, regional, brewpub, large, planning, bar, contract, proprietor, or closed. One of: `0`, `1`, `2`, `3`, `4`, `5`, `6`, `7`, `8`, `9`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `byPostal` | string | no | Filter breweries by postal or ZIP code. Postal+4 may use a hyphen or underscore. |
| `byDistance` | string | no | Sort by distance from an origin point in latitude,longitude format. Do not combine with sort. Example: `35.25738891,-97.46818222`. |
| `byIds` | string | no | Comma-separated list of brewery IDs. Accepts multiple values in one string, delimited by `,`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "address_1": "string",
      "address_2": "string",
      "address_3": "string",
      "brewery_type": "string",
      "city": "string",
      "country": "string",
      "id": "string",
      "latitude": 1,
      "longitude": 1,
      "name": "Ava Chen",
      "phone": "string",
      "postal_code": "string",
      "state": "string",
      "state_province": "string",
      "street": "string",
      "website_url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address_1` | string | Primary street address. |
| `address_2` | string | Secondary address line. |
| `address_3` | string | Third address line. |
| `brewery_type` | string | Type of brewery. |
| `city` | string | City name. |
| `country` | string | Country name. |
| `id` | string | Unique identifier for the brewery. |
| `latitude` | number | Latitude coordinate. |
| `longitude` | number | Longitude coordinate. |
| `name` | string | Brewery name. |
| `phone` | string | Contact phone number. |
| `postal_code` | string | Postal or ZIP code. |
| `state` | string | Deprecated state value. |
| `state_province` | string | State or province. |
| `street` | string | Deprecated street address value. |
| `website_url` | string | Brewery website URL. |

## Native endpoint

Through the native Open Brewery DB API, this operation is `GET /breweries` (base URL `https://api.openbrewerydb.org/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-breweries.md) for the provider-specific parameters and requirements.

