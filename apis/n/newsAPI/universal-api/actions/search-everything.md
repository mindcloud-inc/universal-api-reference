# News API: Search Everything

Finds articles in News API by keyword or phrase.

```
GET https://connect.mindcloud.co/v1/universal/newsAPI/latest/actions/search-everything
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a News API `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/newsAPI/latest/actions/search-everything?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/newsAPI/latest/actions/search-everything?${params}`, {
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
| `domains` | string | no | Comma-separated domains to include. |
| `excludeDomains` | string | no | Comma-separated domains to exclude. |
| `from` | string | no | A date and optional time for the oldest allowed article. |
| `q` | string | no | Keywords or a phrase to search for. |
| `searchIn` | string | no | Restrict the search to article fields such as title, description, or content. |
| `sources` | string | no | Comma-separated source identifiers to search within. |
| `to` | string | no | A date and optional time for the newest allowed article. |
| `language` | string | no | Restrict articles to a single language. One of: `0`, `1`, `10`, `11`, `12`, `2`, `3`, `4`, `5`, `6`, `7`, `8`, `9`. |
| `sortBy` | string | no | Sort order for returned articles. One of: `0`, `1`, `2`. |
| `pageSize` | number | no | Number of results to return per page. |
| `page` | number | no | Page number of the results to return. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "articles": [
        {}
      ],
      "status": "string",
      "totalResults": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `articles` | array<object> | The articles returned by the request. |
| `status` | string | Response status from News API. |
| `totalResults` | number | Total number of matching articles available for the request. |

## Native endpoint

Through the native News API API, this operation is `GET /everything` (base URL `https://newsapi.org/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-everything.md) for the provider-specific parameters and requirements.

