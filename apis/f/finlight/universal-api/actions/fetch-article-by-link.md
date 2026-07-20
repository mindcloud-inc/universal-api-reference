# finlight: Fetch Article By Link

Retrieves a single finlight article by URL.

```
GET https://connect.mindcloud.co/v1/universal/finlight/latest/actions/fetch-article-by-link
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a finlight `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/finlight/latest/actions/fetch-article-by-link?connectionId=$CONNECTION_ID&link=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "link": "https://example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/finlight/latest/actions/fetch-article-by-link?${params}`, {
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
| `link` | string | yes | Article URL to look up. |
| `includeContent` | boolean | no | Include the full article content in the response. |
| `includeEntities` | boolean | no | Include company entities when the subscription tier supports them. |

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

Through the native finlight API, this operation is `GET /v2/articles/by-link` (base URL `https://api.finlight.me`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/fetch-article-by-link.md) for the provider-specific parameters and requirements.

