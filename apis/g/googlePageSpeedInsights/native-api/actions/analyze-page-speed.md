# Analyze Page Speed with Google PageSpeed Insights

Retrieves a Google PageSpeed Insights report for a URL.

## Endpoint

- **Method:** `GET`
- **Path:** `runPagespeed`
- **Base URL:** `https://pagespeedonline.googleapis.com/pagespeedonline/v5`
- **Official documentation:** [Analyze Page Speed](https://developers.google.com/speed/docs/insights/rest/v5/pagespeedapi/runpagespeed)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | query | `string` | yes | Required. The URL to fetch and analyze. |
| `category` | query | `list<string>` | no | Lighthouse category to run. If none are given, Google runs Performance by default. Accepted values: `ACCESSIBILITY`, `BEST_PRACTICES`, `CATEGORY_UNSPECIFIED`, `PERFORMANCE`, `SEO`. Send multiple values as a array. |
| `strategy` | query | `list<string>` | no | Analysis strategy to use. Desktop is the default. Accepted values: `DESKTOP`, `MOBILE`, `STRATEGY_UNSPECIFIED`. |
| `locale` | query | `string` | no | Locale used to localize formatted results. |
| `utm_campaign` | query | `string` | no | Campaign name for analytics. |
| `utm_source` | query | `string` | no | Campaign source for analytics. |
