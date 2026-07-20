# PageVitals: Get Test



```
GET https://connect.mindcloud.co/v1/universal/pageVitals/latest/actions/get-test
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PageVitals `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pageVitals/latest/actions/get-test?connectionId=$CONNECTION_ID&websiteId=string&testId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "websiteId": "string",
  "testId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pageVitals/latest/actions/get-test?${params}`, {
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
| `testId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accessibilityScore": 1,
      "bestPracticesScore": 1,
      "budgetsAtRisk": [
        "string"
      ],
      "budgetsExceeded": [
        "string"
      ],
      "bytesTotal": 1,
      "chromeVersion": "string",
      "cls": 1,
      "cpuTotal": 1,
      "created": "string",
      "device": "string",
      "domElements": 1,
      "domMaxDepth": 1,
      "elapsedSec": 1,
      "fcp": 1,
      "lcp": 1,
      "lighthouseVersion": "string",
      "location": "string",
      "opportunities": [
        "string"
      ],
      "pageAlias": "string",
      "pageId": "string",
      "performanceScore": 1,
      "runner": "string",
      "seoScore": 1,
      "seriesId": "string",
      "speedIndex": 1,
      "status": "string",
      "tbt": 1,
      "testId": "string",
      "tti": 1,
      "url": "https://example.com",
      "website": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accessibilityScore` | number |  |
| `bestPracticesScore` | number |  |
| `budgetsAtRisk` | array<string> |  |
| `budgetsExceeded` | array<string> |  |
| `bytesTotal` | number |  |
| `chromeVersion` | string |  |
| `cls` | number |  |
| `cpuTotal` | number |  |
| `created` | string |  |
| `device` | string |  |
| `domElements` | number |  |
| `domMaxDepth` | number |  |
| `elapsedSec` | number |  |
| `fcp` | number |  |
| `lcp` | number |  |
| `lighthouseVersion` | string |  |
| `location` | string |  |
| `opportunities` | array<string> |  |
| `pageAlias` | string |  |
| `pageId` | string |  |
| `performanceScore` | number |  |
| `runner` | string |  |
| `seoScore` | number |  |
| `seriesId` | string |  |
| `speedIndex` | number |  |
| `status` | string |  |
| `tbt` | number |  |
| `testId` | string |  |
| `tti` | number |  |
| `url` | string |  |
| `website` | string |  |

## Native endpoint

Through the native PageVitals API, this operation is `GET /:websiteId/tests/:testId` (base URL `https://api.pagevitals.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-test.md) for the provider-specific parameters and requirements.

