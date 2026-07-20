# Google PageSpeed Insights: Analyze Page Speed

Retrieves a Google PageSpeed Insights report for a URL.

```
GET https://connect.mindcloud.co/v1/universal/googlePageSpeedInsights/latest/actions/analyze-page-speed
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google PageSpeed Insights `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/googlePageSpeedInsights/latest/actions/analyze-page-speed?connectionId=$CONNECTION_ID&url=https%3A%2F%2Fweb.dev%2F" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "url": "https://web.dev/"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/googlePageSpeedInsights/latest/actions/analyze-page-speed?${params}`, {
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
| `url` | string | yes | Required. The URL to fetch and analyze. Example: `https://web.dev/`. |
| `category` | list<string> | no | Lighthouse category to run. If none are given, Google runs Performance by default. One of: `ACCESSIBILITY`, `BEST_PRACTICES`, `CATEGORY_UNSPECIFIED`, `PERFORMANCE`, `SEO`. Accepts multiple values as an array. Default: `PERFORMANCE`. Example: `PERFORMANCE`. |
| `strategy` | list<string> | no | Analysis strategy to use. Desktop is the default. One of: `DESKTOP`, `MOBILE`, `STRATEGY_UNSPECIFIED`. Default: `DESKTOP`. Example: `DESKTOP`. |
| `locale` | string | no | Locale used to localize formatted results. Example: `en-US`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `utmCampaign` | string | no | Campaign name for analytics. Example: `weekly-report`. |
| `utmSource` | string | no | Campaign source for analytics. Example: `mindcloud`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "analysisUTCTimestamp": "2026-05-07T12:00:00.000Z",
      "captchaResult": "string",
      "id": "string",
      "kind": "string",
      "lighthouseResult": {
        "categories": {
          "accessibility": {
            "score": 1
          },
          "best-practices": {
            "score": 1
          },
          "performance": {
            "score": 1
          },
          "seo": {
            "score": 1
          }
        },
        "fetchTime": "2026-05-07T12:00:00.000Z",
        "finalDisplayedUrl": "https://example.com",
        "finalUrl": "https://example.com",
        "lighthouseVersion": "string",
        "requestedUrl": "https://example.com",
        "runtimeError": {},
        "userAgent": "string"
      },
      "loadingExperience": {
        "overall_category": "string"
      },
      "originLoadingExperience": {
        "overall_category": "string"
      },
      "version": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `analysisUTCTimestamp` | date | UTC timestamp of the analysis. |
| `captchaResult` | string | Captcha verification result. |
| `id` | string | Canonicalized and final URL for the analyzed document. |
| `kind` | string | Kind of PageSpeed result. |
| `lighthouseResult` | object | Lighthouse audit result object for the analyzed URL. |
| `lighthouseResult.categories` | object | Lighthouse category results keyed by category. |
| `lighthouseResult.categories.accessibility.score` | number | Accessibility category score when that category is requested. |
| `lighthouseResult.categories.best-practices.score` | number | Best practices category score when that category is requested. |
| `lighthouseResult.categories.performance.score` | number | Performance category score when the performance category is present. |
| `lighthouseResult.categories.seo.score` | number | SEO category score when that category is requested. |
| `lighthouseResult.fetchTime` | date | Fetch timestamp recorded by Lighthouse. |
| `lighthouseResult.finalDisplayedUrl` | string | Displayed final URL. |
| `lighthouseResult.finalUrl` | string | Final URL after redirects. |
| `lighthouseResult.lighthouseVersion` | string | Lighthouse version used for the run. |
| `lighthouseResult.requestedUrl` | string | URL requested for analysis. |
| `lighthouseResult.runtimeError` | object | Runtime error details when Lighthouse could not complete normally. |
| `lighthouseResult.userAgent` | string | User agent used by Lighthouse. |
| `loadingExperience` | object | Field data metrics for the analyzed page URL. |
| `loadingExperience.overall_category` | string | Overall field-data loading category for the page URL. |
| `originLoadingExperience` | object | Aggregated field data metrics for the page origin. |
| `originLoadingExperience.overall_category` | string | Overall field-data loading category for the origin. |
| `version` | object | PageSpeed version information. |

## Native endpoint

Through the native Google PageSpeed Insights API, this operation is `GET runPagespeed` (base URL `https://pagespeedonline.googleapis.com/pagespeedonline/v5`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/analyze-page-speed.md) for the provider-specific parameters and requirements.

