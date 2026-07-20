# SharpAPI: Scrape URL Content

Scrapes content from a URL with SharpAPI.

```
POST https://connect.mindcloud.co/v1/universal/sharpAPI/latest/actions/scrape-url-content
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SharpAPI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/sharpAPI/latest/actions/scrape-url-content" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "url": "https://sharpapi.com/"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sharpAPI/latest/actions/scrape-url-content', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "url": "https://sharpapi.com/"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `url` | string | yes | Public URL to scrape. Example: `https://sharpapi.com/`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "scraped_data": {
        "content_markdown": "string",
        "detected_language": "string",
        "links": {
          "external": [
            "https://example.com"
          ],
          "internal": [
            "https://example.com"
          ]
        },
        "title": "string"
      },
      "timestamp": "2026-05-07T12:00:00.000Z",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `scraped_data.content_markdown` | string | Main scraped page content rendered as markdown. |
| `scraped_data.detected_language` | string | Detected page language. |
| `scraped_data.links.external` | array<string> | External links discovered on the page. |
| `scraped_data.links.internal` | array<string> | Internal links discovered on the page. |
| `scraped_data.title` | string | Page title extracted from the URL. |
| `timestamp` | date | Timestamp when SharpAPI scraped the page. |
| `url` | string | URL that was scraped. |

## Native endpoint

Through the native SharpAPI API, this operation is `GET /utilities/scrape_url` (base URL `https://sharpapi.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/scrape-url-content.md) for the provider-specific parameters and requirements.

