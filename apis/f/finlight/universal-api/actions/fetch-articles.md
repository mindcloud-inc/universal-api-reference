# finlight: Fetch Articles

Finds financial news articles in finlight.

```
GET https://connect.mindcloud.co/v1/universal/finlight/latest/actions/fetch-articles
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a finlight `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/finlight/latest/actions/fetch-articles?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/finlight/latest/actions/fetch-articles?${params}`, {
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
| `query` | string | no | Search query with optional advanced field filters. |
| `tickers[]` | array<string> | no | Filter articles by stock ticker symbols. |
| `sources[]` | array<string> | no | Filter articles by source domain list. |
| `excludeSources[]` | array<string> | no | Exclude source domains from the results. |
| `countries[]` | array<string> | no | Filter articles by ISO 3166-1 alpha-2 country codes. |
| `language` | string | no | Filter results by ISO 639-1 language code. |
| `from` | string | no | Start date in YYYY-MM-DD format or ISO datetime. |
| `to` | string | no | End date in YYYY-MM-DD format or ISO datetime. |
| `includeEntities` | boolean | no | Include company entities when the subscription tier supports them. |
| `orderBy` | string | no | Sort field: publishDate or createdAt. Default: `publishDate`. |
| `order` | string | no | Sort direction: ASC or DESC. Default: `DESC`. |
| `pageSize` | number | no | Number of results per page. |
| `page` | number | no | Page number. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "categories": [
        "string"
      ],
      "countries": [
        "string"
      ],
      "images": [
        "string"
      ],
      "language": "string",
      "link": "https://example.com",
      "publishDate": "2026-05-07T12:00:00.000Z",
      "source": "string",
      "summary": "string",
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `categories` | array<string> | Article category labels. |
| `countries` | array<string> | Country codes associated with the article. |
| `images` | array<string> | Image URLs returned for the article. |
| `language` | string | Language code for the article. |
| `link` | string | Canonical article URL. |
| `publishDate` | date | Article publication timestamp. |
| `source` | string | Source domain for the article. |
| `summary` | string | Article summary text. |
| `title` | string | Article title. |

## Native endpoint

Through the native finlight API, this operation is `POST /v2/articles` (base URL `https://api.finlight.me`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/fetch-articles.md) for the provider-specific parameters and requirements.

