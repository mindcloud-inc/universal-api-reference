# Get Ad Statistics with LinkedIn Ads Reports

Retrieves ad statistics from LinkedIn Ads Reports.

## Endpoint

- **Method:** `GET`
- **Path:** `/rest/adAnalytics?q=statistics&pivots={{pivots}}&dateRange=(start:(year:{{startYear}},month:{{startMonth}},day:{{startDay}}),end:(year:{{endYear}},month:{{endMonth}},day:{{endDay}}))&timeGranularity={{timeGranularity}}&{{facet}}`
- **Base URL:** `https://api.linkedin.com`
- **Official documentation:** [Get Ad Statistics](https://learn.microsoft.com/en-us/linkedin/marketing/integrations/ads-reporting/ads-reporting?view=li-lms-2026-03)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `pivots` | path | `string` | yes | LinkedIn Rest.li pivot list, for example List(ACCOUNT). |
| `facet` | path | `string` | yes | LinkedIn reporting facet expression, for example accounts=List(urn%3Ali%3AsponsoredAccount%3A123456). |
| `startYear` | path | `number` | yes | Start date year. |
| `startMonth` | path | `number` | yes | Start date month. |
| `startDay` | path | `number` | yes | Start date day. |
| `endYear` | path | `number` | yes | End date year. |
| `endMonth` | path | `number` | yes | End date month. |
| `endDay` | path | `number` | yes | End date day. |
| `timeGranularity` | path | `string` | yes | Time grouping for the report, such as DAILY or ALL. |
