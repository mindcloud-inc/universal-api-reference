# Perigon: Search Companies

Finds companies in Perigon by name, symbol, or domain.

```
GET https://connect.mindcloud.co/v1/universal/perigon/latest/actions/search-companies
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Perigon `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/perigon/latest/actions/search-companies?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/perigon/latest/actions/search-companies?${params}`, {
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
| `q` | string | no | Example: `semiconductors`. |
| `id` | string | no | Accepts multiple values in one string, delimited by `,`. Example: `company_123`. |
| `symbol` | string | no | Accepts multiple values in one string, delimited by `,`. Example: `NVDA`. |
| `domain` | string | no | Accepts multiple values in one string, delimited by `,`. Example: `nvidia.com`. |
| `country` | string | no | Accepts multiple values in one string, delimited by `,`. Example: `us`. |
| `exchange` | string | no | Accepts multiple values in one string, delimited by `,`. Example: `NASDAQ`. |
| `numEmployeesFrom` | number | no | Example: `1000`. |
| `numEmployeesTo` | number | no | Example: `100000`. |
| `ipoFrom` | date | no | Example: `2000-01-01T00:00:00`. |
| `ipoTo` | date | no | Example: `2026-04-09T23:59:59`. |
| `name` | string | no | Example: `NVIDIA`. |
| `industry` | string | no | Example: `Semiconductors`. |
| `sector` | string | no | Example: `Technology`. |
| `size` | number | no | Example: `10`. |
| `page` | number | no | Example: `0`. |

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

Through the native Perigon API, this operation is `GET /v1/companies/all` (base URL `https://api.perigon.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/search-companies.md) for the provider-specific parameters and requirements.

