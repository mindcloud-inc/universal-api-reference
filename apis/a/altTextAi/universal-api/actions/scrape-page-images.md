# AltText.Ai: Scrape Page Images

Scrapes page images for alt text generation in AltText.Ai.

```
POST https://connect.mindcloud.co/v1/universal/altTextAi/latest/actions/scrape-page-images
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AltText.Ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/altTextAi/latest/actions/scrape-page-images" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "pageScrape": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/altTextAi/latest/actions/scrape-page-images', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "pageScrape": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `includeExisting` | boolean | no | When true, also process images that already have alt text. |
| `keywords[]` | array<string> | no | Optional SEO keywords or phrases for generated alt text on each scraped image. |
| `lang` | string | no | One or more language codes for generated alt text. |
| `negativeKeywords[]` | array<string> | no | Optional keywords or phrases to avoid in generated alt text. |
| `pageScrape` | object | yes | Provide the page URL to scrape, or raw HTML, inside this object. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "errors": {},
      "scrapedImages": [
        {}
      ],
      "totalProcessed": 1,
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `errors` | object |  |
| `scrapedImages` | array<object> |  |
| `totalProcessed` | number |  |
| `url` | string |  |

## Native endpoint

Through the native AltText.Ai API, this operation is `POST /images/page_scrape` (base URL `https://alttext.ai/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/scrape-page-images.md) for the provider-specific parameters and requirements.

