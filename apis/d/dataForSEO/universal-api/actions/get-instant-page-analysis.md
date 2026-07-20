# DataForSEO: Get Instant Page Analysis

Retrieves instant page analysis from DataForSEO.

```
GET https://connect.mindcloud.co/v1/universal/dataForSEO/latest/actions/get-instant-page-analysis
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DataForSEO `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dataForSEO/latest/actions/get-instant-page-analysis?connectionId=$CONNECTION_ID&url=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "url": "https://example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dataForSEO/latest/actions/get-instant-page-analysis?${params}`, {
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
| `url` | string | yes | URL of the page to analyze. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `enable_javascript` | boolean | no | Enable JavaScript rendering for the page. |
| `custom_js` | string | no | Custom JavaScript code to execute. |
| `custom_user_agent` | string | no | Custom User-Agent header value. |
| `accept_language` | string | no | Language header value for accessing the website. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "checks": {},
      "contentEncoding": "string",
      "fetchTime": "string",
      "lastModified": {},
      "mediaType": "string",
      "meta": {},
      "onpageScore": 1,
      "pageTiming": {},
      "relativeUrlLength": 1,
      "resourceType": "string",
      "server": "string",
      "size": 1,
      "statusCode": 1,
      "totalDomSize": 1,
      "url": "https://example.com",
      "urlLength": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `checks` | object | Boolean on-page checks reported by the provider. |
| `contentEncoding` | string | Content encoding reported by the provider. |
| `fetchTime` | string | Provider fetch timestamp. |
| `lastModified` | object | Last-modified header details when available. |
| `mediaType` | string | Media type reported by the provider. |
| `meta` | object | Page metadata including title and content metrics. |
| `onpageScore` | number | Overall on-page score returned by DataForSEO. |
| `pageTiming` | object | Timing metrics returned by the on-page analysis. |
| `relativeUrlLength` | number | Relative URL length metric. |
| `resourceType` | string | Detected response resource type. |
| `server` | string | Server header observed during the fetch. |
| `size` | number | Document size in bytes. |
| `statusCode` | number | HTTP status code observed when DataForSEO fetched the page. |
| `totalDomSize` | number | Total DOM size reported for the page. |
| `url` | string | Normalized page URL analyzed by the endpoint. |
| `urlLength` | number | Absolute URL length metric. |

## Native endpoint

Through the native DataForSEO API, this operation is `POST /v3/on_page/instant_pages.ai` (base URL `https://api.dataforseo.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-instant-page-analysis.md) for the provider-specific parameters and requirements.

