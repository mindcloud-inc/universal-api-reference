# <img src="https://images.mindcloud.co/apps/icons/google-page-speed-insights_1776793656423.png" alt="Google PageSpeed Insights logo" width="28" height="28"> Google PageSpeed Insights: Universal API

Analyze web page performance with Google PageSpeed Insights and Lighthouse data, including performance, accessibility, best practices, and SEO results.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/googlePageSpeedInsights/latest
- **Category:** IT Operations / Developer Tools
- **Actions:** 1
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://pagespeed.web.dev/
- **Vendor API docs:** https://developers.google.com/speed/docs/insights/v5/get-started

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Analyze Page Speed](actions/analyze-page-speed.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/googlePageSpeedInsights/latest/actions/analyze-page-speed?connectionId=$CONNECTION_ID&url=https%3A%2F%2Fweb.dev%2F" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (1)

### Pagespeed Analysis

| Action | Method | Description |
| --- | --- | --- |
| [Analyze Page Speed](actions/analyze-page-speed.md) | GET | Retrieves a Google PageSpeed Insights report for a URL. |

