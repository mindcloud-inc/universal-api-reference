# Perigon: Search Sources

Finds media sources in Perigon by attributes and filters.

```
GET https://connect.mindcloud.co/v1/universal/perigon/latest/actions/search-sources
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Perigon `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/perigon/latest/actions/search-sources?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/perigon/latest/actions/search-sources?${params}`, {
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
| `domain` | string | no | Accepts multiple values in one string, delimited by `,`. Example: `nytimes.com`. |
| `name` | string | no | Example: `New York Times`. |
| `sourceGroup` | string | no | Accepts multiple values in one string, delimited by `,`. Example: `top100`. |
| `sortBy` | string | no | Example: `monthlyVisits`. |
| `page` | number | no | Example: `0`. |
| `size` | number | no | Example: `10`. |
| `minMonthlyVisits` | number | no | Example: `100000`. |
| `maxMonthlyVisits` | number | no | Example: `5000000`. |
| `country` | string | no | Accepts multiple values in one string, delimited by `,`. Example: `us`. |
| `sourceCountry` | string | no | Accepts multiple values in one string, delimited by `,`. Example: `us`. |
| `sourceState` | string | no | Accepts multiple values in one string, delimited by `,`. Example: `ca`. |
| `sourceCity` | string | no | Accepts multiple values in one string, delimited by `,`. Example: `San Francisco`. |
| `category` | string | no | Accepts multiple values in one string, delimited by `,`. Example: `Tech`. |
| `topic` | string | no | Accepts multiple values in one string, delimited by `,`. Example: `Artificial Intelligence`. |
| `label` | string | no | Accepts multiple values in one string, delimited by `,`. Example: `Opinion`. |
| `paywall` | boolean | no |  |
| `showNumResults` | boolean | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "numResults": 1,
      "results": [
        {}
      ],
      "status": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `numResults` | number |  |
| `results` | array<object> |  |
| `status` | number |  |

## Native endpoint

Through the native Perigon API, this operation is `GET /v1/sources/all` (base URL `https://api.perigon.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/search-sources.md) for the provider-specific parameters and requirements.

