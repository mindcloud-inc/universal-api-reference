# Scrapi: Scrape Website

Creates a website scrape job in Scrapi.

```
POST https://connect.mindcloud.co/v1/universal/scrapi/latest/actions/scrape-website
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Scrapi `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/scrapi/latest/actions/scrape-website" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/scrapi/latest/actions/scrape-website', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `useBrowser` | string | no | Use a full headless browser with JavaScript execution. |
| `responseFormat` | string | no | Response format: Json, Html, or Markdown. Default: `Json`. |
| `responseFormat` | string | no | Response format: Json, Html, or Markdown. Default: `Json`. |
| `responseSelector` | string | no | CSS or XPath selector for extracted content. |
| `responseSelector` | string | no | CSS or XPath selector for extracted content. |
| `requestMethod` | string | no | Target request method for the scrape request. Default: `GET`. |
| `requestMethod` | string | no | Target request method for the scrape request. Default: `GET`. |
| `requestBodyBase64` | string | no | Base64-encoded body for POST target requests. |
| `requestBodyBase64` | string | no | Base64-encoded body for POST target requests. |
| `useBrowser` | boolean | no | Use a full headless browser with JavaScript execution. |
| `solveCaptchas` | boolean | no | Attempt captcha solving during the scrape. |
| `includeScreenshot` | boolean | no | Include a screenshot in the scrape response. |
| `includePdf` | boolean | no | Include a PDF capture in the scrape response. |
| `includeVideo` | boolean | no | Include a video capture in the scrape response. |
| `acceptDialogs` | boolean | no | Accept popup dialogs instead of cancelling them. |
| `cookies` | object | no | Custom cookies as key/value pairs. |
| `headers` | object | no | Custom headers as key/value pairs. |
| `proxyType` | string | no | Proxy type: None, Free, Residential, DataCenter, Tor, or Custom. Default: `None`. |
| `proxyCountry` | string | no | Proxy country key used when geotargeting. |
| `proxyCity` | string | no | Proxy city key used when geotargeting. |
| `customProxyUrl` | string | no | Custom proxy URL used when proxy type is Custom. |
| `sessionId` | string | no | Session identifier to persist state across requests. |
| `callbackUrl` | string | no | Webhook URL to receive the response asynchronously. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "reference": "string",
      "status": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `reference` | string |  |
| `status` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Scrapi API, this operation is `POST /v1/scrape` (base URL `https://api.scrapi.tech`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/scrape-website.md) for the provider-specific parameters and requirements.

