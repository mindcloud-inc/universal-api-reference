# HasData: Scrape Web Page

Retrieves scraped web page data from HasData.

```
GET https://connect.mindcloud.co/v1/universal/hasData/latest/actions/scrape-web-page
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HasData `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hasData/latest/actions/scrape-web-page?connectionId=$CONNECTION_ID&url=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "url": "https://example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hasData/latest/actions/scrape-web-page?${params}`, {
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
| `extractEmails` | boolean | no | Extract email addresses found on the page. |
| `extractLinks` | boolean | no | Extract links found on the page. |
| `outputFormat[]` | array<string> | no | Formats to include in the response. |
| `proxyCountry` | string | no | ISO alpha-2 country code for the proxy. |
| `proxyType` | string | no | Proxy type to use for the request. |
| `screenshot` | boolean | no | Include a rendered page screenshot. |
| `url` | string | yes | The public page URL to scrape. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "content": "string",
      "cookies": [
        {}
      ],
      "headers": {},
      "markdown": "string",
      "requestMetadata": {},
      "screenshot": "string",
      "text": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `content` | string | Raw HTML content. |
| `cookies` | array<object> | Cookies returned by the target page. |
| `headers` | object | Response headers from the target page. |
| `markdown` | string | Markdown extraction. |
| `requestMetadata` | object | Request execution metadata. |
| `screenshot` | string | Screenshot URL when requested. |
| `text` | string | Plain text extraction. |

## Native endpoint

Through the native HasData API, this operation is `POST /scrape/web` (base URL `https://api.hasdata.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/scrape-web-page.md) for the provider-specific parameters and requirements.

