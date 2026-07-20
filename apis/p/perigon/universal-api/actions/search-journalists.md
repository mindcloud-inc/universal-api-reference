# Perigon: Search Journalists

Finds journalists in Perigon by name, source, or topic.

```
GET https://connect.mindcloud.co/v1/universal/perigon/latest/actions/search-journalists
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Perigon `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/perigon/latest/actions/search-journalists?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/perigon/latest/actions/search-journalists?${params}`, {
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
| `q` | string | no | Example: `renewable energy`. |
| `id` | string | no | Accepts multiple values in one string, delimited by `,`. Example: `journalist_123`. |
| `name` | string | no | Example: `Kevin Roose`. |
| `twitter` | string | no | Example: `kevinroose`. |
| `page` | number | no | Example: `0`. |
| `size` | number | no | Example: `10`. |
| `source` | string | no | Accepts multiple values in one string, delimited by `,`. Example: `nytimes.com`. |
| `topic` | string | no | Accepts multiple values in one string, delimited by `,`. Example: `Energy`. |
| `category` | string | no | Accepts multiple values in one string, delimited by `,`. Example: `Business`. |
| `label` | string | no | Accepts multiple values in one string, delimited by `,`. Example: `Opinion`. |
| `minMonthlyPosts` | number | no | Example: `5`. |
| `maxMonthlyPosts` | number | no | Example: `100`. |
| `country` | string | no | Accepts multiple values in one string, delimited by `,`. Example: `us`. |
| `updatedAtFrom` | date | no | Example: `2026-04-01T00:00:00`. |
| `updatedAtTo` | date | no | Example: `2026-04-09T23:59:59`. |
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

Through the native Perigon API, this operation is `GET /v1/journalists/all` (base URL `https://api.perigon.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/search-journalists.md) for the provider-specific parameters and requirements.

