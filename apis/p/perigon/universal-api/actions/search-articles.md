# Perigon: Search Articles

Finds news articles in Perigon by keywords and filters.

```
GET https://connect.mindcloud.co/v1/universal/perigon/latest/actions/search-articles
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Perigon `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/perigon/latest/actions/search-articles?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/perigon/latest/actions/search-articles?${params}`, {
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
| `q` | string | no | Example: `artificial intelligence`. |
| `articleId` | string | no | Accepts multiple values in one string, delimited by `,`. Example: `article_123`. |
| `clusterId` | string | no | Accepts multiple values in one string, delimited by `,`. Example: `cluster_123`. |
| `sortBy` | string | no | Example: `date`. |
| `page` | number | no | Example: `0`. |
| `size` | number | no | Example: `10`. |
| `from` | date | no | Example: `2026-04-01T00:00:00`. |
| `to` | date | no | Example: `2026-04-09T23:59:59`. |
| `source` | string | no | Accepts multiple values in one string, delimited by `,`. Example: `nytimes.com`. |
| `sourceGroup` | string | no | Accepts multiple values in one string, delimited by `,`. Example: `top100`. |
| `language` | string | no | Accepts multiple values in one string, delimited by `,`. Example: `en`. |
| `category` | string | no | Accepts multiple values in one string, delimited by `,`. Example: `Tech`. |
| `topic` | string | no | Accepts multiple values in one string, delimited by `,`. Example: `Artificial Intelligence`. |
| `country` | string | no | Accepts multiple values in one string, delimited by `,`. Example: `us`. |
| `journalistId` | string | no | Accepts multiple values in one string, delimited by `,`. Example: `journalist_123`. |
| `companyName` | string | no | Example: `OpenAI`. |
| `showNumResults` | boolean | no |  |
| `showReprints` | boolean | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "articles": [
        {}
      ],
      "numResults": 1,
      "status": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `articles` | array<object> |  |
| `numResults` | number |  |
| `status` | number |  |

## Native endpoint

Through the native Perigon API, this operation is `GET /v1/articles/all` (base URL `https://api.perigon.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/search-articles.md) for the provider-specific parameters and requirements.

