# PageVitals: Get Page Timeline



```
GET https://connect.mindcloud.co/v1/universal/pageVitals/latest/actions/get-page-timeline
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PageVitals `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pageVitals/latest/actions/get-page-timeline?connectionId=$CONNECTION_ID&websiteId=string&pageId=string&device=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "websiteId": "string",
  "pageId": "string",
  "device": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pageVitals/latest/actions/get-page-timeline?${params}`, {
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
| `websiteId` | string | yes |  |
| `pageId` | string | yes |  |
| `device` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "cls": 1,
      "connectTime": 1,
      "count": 1,
      "date": "string",
      "dnsTime": 1,
      "domElements": 1,
      "domMaxDepth": 1,
      "domReady": 1,
      "fcp": 1,
      "lcp": 1,
      "onLoad": 1,
      "serverTime": 1,
      "speedIndex": 1,
      "tbt": 1,
      "transferTime": 1,
      "ttfb": 1,
      "tti": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cls` | number |  |
| `connectTime` | number |  |
| `count` | number |  |
| `date` | string |  |
| `dnsTime` | number |  |
| `domElements` | number |  |
| `domMaxDepth` | number |  |
| `domReady` | number |  |
| `fcp` | number |  |
| `lcp` | number |  |
| `onLoad` | number |  |
| `serverTime` | number |  |
| `speedIndex` | number |  |
| `tbt` | number |  |
| `transferTime` | number |  |
| `ttfb` | number |  |
| `tti` | number |  |

## Native endpoint

Through the native PageVitals API, this operation is `GET /:websiteId/pages/:pageId/timeline` (base URL `https://api.pagevitals.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-page-timeline.md) for the provider-specific parameters and requirements.

