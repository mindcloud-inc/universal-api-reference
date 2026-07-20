# Browserless: Smart Scrape Url

Retrieves structured page data from a URL in Browserless.

```
GET https://connect.mindcloud.co/v1/universal/browserless/latest/actions/smart-scrape-url
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Browserless `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/browserless/latest/actions/smart-scrape-url?connectionId=$CONNECTION_ID&url=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "url": "https://example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/browserless/latest/actions/smart-scrape-url?${params}`, {
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
| `url` | string | yes | The URL to scrape. Must be an http or https URL. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `formats[]` | array<string> | no | Optional output formats to include in the smart scrape response. |
| `timeout` | number | no | Optional timeout in milliseconds for the smart scrape request. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attempted": [
        "string"
      ],
      "content": "string",
      "contentType": "string",
      "headers": {},
      "ok": true,
      "statusCode": 1,
      "strategy": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attempted` | array<string> | Ordered list of Browserless strategies attempted for the request. |
| `content` | string | Captured page content returned by Browserless for the requested URL. |
| `contentType` | string | Content type reported for the captured content payload. |
| `headers` | object | Response headers observed by Browserless when fetching the target URL. |
| `ok` | boolean | Whether Browserless successfully completed the smart scrape request. |
| `statusCode` | number | HTTP-style status code returned by Browserless for the scrape result. |
| `strategy` | string | Browserless fetch strategy used to satisfy the smart scrape request. |

## Native endpoint

Through the native Browserless API, this operation is `POST /smart-scrape` (base URL `https://production-sfo.browserless.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/smart-scrape-url.md) for the provider-specific parameters and requirements.

