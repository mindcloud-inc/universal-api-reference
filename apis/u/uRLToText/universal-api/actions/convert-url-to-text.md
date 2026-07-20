# URL to Text: Convert URL to Text

Retrieves extracted webpage or YouTube content from URL to Text.

```
GET https://connect.mindcloud.co/v1/universal/uRLToText/latest/actions/convert-url-to-text
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a URL to Text `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/uRLToText/latest/actions/convert-url-to-text?connectionId=$CONNECTION_ID&url=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "url": "https://example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/uRLToText/latest/actions/convert-url-to-text?${params}`, {
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
| `url` | string | yes | The webpage or YouTube URL to convert. Example: `https://example.com`. |
| `outputFormat` | list<string> | no | The format to return. URLtoText supports text, markdown, and html. One of: `0`, `1`, `2`. Default: `text`. |
| `extractMainContent` | boolean | no | Use URLtoText's AI extraction to attempt to return only the main content. Default: `false`. |
| `renderJavascript` | boolean | no | Render JavaScript before extracting content. Default: `false`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `residentialProxy` | boolean | no | Use a residential proxy for the request. Only one proxy option should be enabled at a time. Default: `false`. |
| `stealthProxy` | boolean | no | Use URLtoText's premium residential IP pool. Requires JavaScript rendering. Default: `false`. |
| `aiPrompt` | string | no | Optional AI prompt to process or modify the extracted content. |
| `endOfArticle` | string | no | Optional text marker where extraction should stop. |
| `waitForJs` | number | no | Milliseconds to wait for JavaScript to finish loading before extraction. Example: `3000`. |
| `extractCssSelector` | string | no | One or more CSS selectors separated by commas. If omitted or unmatched, the whole page is processed. Example: `#main-content, .article`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "content": "string",
      "creditsUsed": 1,
      "ogDescription": "string",
      "ogImageUrl": "https://example.com",
      "outputFormat": "string",
      "pageTitle": "string",
      "publishedDate": "2026-05-07T12:00:00.000Z",
      "url": "https://example.com",
      "warning": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `content` | string | Extracted page content. |
| `creditsUsed` | number | URLtoText credits consumed by the conversion. |
| `ogDescription` | string | Open Graph description, when available. |
| `ogImageUrl` | string | Open Graph image URL, when available. |
| `outputFormat` | string | Returned content format. |
| `pageTitle` | string | Title of the source page. |
| `publishedDate` | date | Detected publication date, when available. |
| `url` | string | The URL that was converted. |
| `warning` | string | Provider warning message, when returned. |

## Native endpoint

Through the native URL to Text API, this operation is `POST /urltotext/` (base URL `https://urltotext.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/convert-url-to-text.md) for the provider-specific parameters and requirements.

