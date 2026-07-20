# Firecrawl: Extract Data

Creates a data extraction job in Firecrawl.

```
POST https://connect.mindcloud.co/v1/universal/firecrawl/latest/actions/extract-data
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Firecrawl `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/firecrawl/latest/actions/extract-data" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "urls[]": [
    "https://example.com"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/firecrawl/latest/actions/extract-data', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "urls[]": ["https://example.com"]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `urls[]` | array<string> | yes | The URLs to extract data from |
| `prompt` | string | no | Prompt to guide the extraction process |
| `schema` | object | no | JSON Schema defining the structure of the extracted data |
| `enableWebSearch` | boolean | no | Use web search to find additional data |
| `ignoreSitemap` | boolean | no | Ignore sitemap.xml files during website scanning |
| `includeSubdomains` | boolean | no | Scan subdomains of the provided URLs |
| `showSources` | boolean | no | Include the sources used to extract the data |
| `scrapeOptions` | object | no | Scrape options to use during extraction |
| `ignoreInvalidURLs` | boolean | no | Ignore invalid URLs instead of failing the entire extract request |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "urlTrace": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `urlTrace` | array<object> |  |

## Native endpoint

Through the native Firecrawl API, this operation is `POST /extract` (base URL `https://api.firecrawl.dev/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/extract-data.md) for the provider-specific parameters and requirements.

