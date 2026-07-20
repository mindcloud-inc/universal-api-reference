# News API: List Top Headlines

Finds top headlines in News API by country, category, or source.

```
GET https://connect.mindcloud.co/v1/universal/newsAPI/latest/actions/list-top-headlines
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a News API `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/newsAPI/latest/actions/list-top-headlines?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/newsAPI/latest/actions/list-top-headlines?${params}`, {
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
| `country` | string | no | Two-letter ISO 3166-1 country code to fetch headlines for. One of: `0`. |
| `q` | string | no | Keywords or a phrase to search for. Defaults to `news` when no other top-headlines filter is supplied. Default: `news`. |
| `sources` | string | no | Comma-separated source identifiers to fetch headlines from. |
| `category` | string | no | Category of headlines to return. One of: `0`, `1`, `2`, `3`, `4`, `5`, `6`. |
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
| `articles` | array<object> | The top headline articles returned by the request. |
| `status` | string | Response status from News API. |
| `totalResults` | number | Total number of matching headlines available for the request. |

## Native endpoint

Through the native News API API, this operation is `GET /top-headlines` (base URL `https://newsapi.org/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-top-headlines.md) for the provider-specific parameters and requirements.

