# Google PageSpeed Insights Universal API Examples

These examples use the MindCloud API key and Google PageSpeed Insights connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Analyze Page Speed

Retrieves a Google PageSpeed Insights report for a URL.

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

Example response:

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

See the full [Analyze Page Speed action reference](actions/analyze-page-speed.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/googlePageSpeedInsights/latest/actions/analyze-page-speed).
