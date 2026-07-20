# List Latest Visits (100/200/500) with ShinyStat

Retrieves the latest 100, 200, or 500 visits from ShinyStat.

## Endpoint

- **Method:** `POST`
- **Path:** `/ajax`
- **Base URL:** `https://report.shinystat.com`
- **Official documentation:** [List Latest Visits (100/200/500)](https://www.shinystat.com/it/guida-elemento_report-generale-ultime-100-300-visite.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `href` | body | `string` | yes | Temporary default route for this report. Replace with the exact internal ShinyStat report route once authenticated dashboard evidence is available. |
