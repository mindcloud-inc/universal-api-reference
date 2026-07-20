# Open Brewery DB: Get Brewery Metadata

Retrieves brewery metadata from Open Brewery DB.

```
GET https://connect.mindcloud.co/v1/universal/openBreweryDB/latest/actions/get-brewery-metadata
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Open Brewery DB `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/openBreweryDB/latest/actions/get-brewery-metadata?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/openBreweryDB/latest/actions/get-brewery-metadata?${params}`, {
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
| `byCity` | string | no | Filter brewery metadata by city. Use underscores or URL encoding for spaces. |
| `byCountry` | string | no | Filter brewery metadata by country. Use underscores or URL encoding for spaces. |
| `byName` | string | no | Filter brewery metadata by name. Use underscores or URL encoding for spaces. |
| `byState` | string | no | Filter brewery metadata by full state name; abbreviations are not supported. |
| `byType` | list | no | Filter metadata by brewery type: micro, nano, regional, brewpub, large, planning, bar, contract, proprietor, or closed. One of: `0`, `1`, `2`, `3`, `4`, `5`, `6`, `7`, `8`, `9`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `byPostal` | string | no | Filter brewery metadata by postal or ZIP code. Postal+4 may use a hyphen or underscore. |
| `byDistance` | string | no | Sort/filter metadata by distance from an origin point in latitude,longitude format. Example: `35.25738891,-97.46818222`. |
| `byIds` | string | no | Comma-separated list of brewery IDs for metadata filtering. Accepts multiple values in one string, delimited by `,`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "by_state": {},
      "by_type": {},
      "page": 1,
      "per_page": 1,
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `by_state` | object | Counts grouped by state or province. |
| `by_type` | object | Counts grouped by brewery type. |
| `page` | number | Current page number. |
| `per_page` | number | Number of breweries per page. |
| `total` | number | Total number of breweries matching the filters. |

## Native endpoint

Through the native Open Brewery DB API, this operation is `GET /breweries/meta` (base URL `https://api.openbrewerydb.org/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-brewery-metadata.md) for the provider-specific parameters and requirements.

