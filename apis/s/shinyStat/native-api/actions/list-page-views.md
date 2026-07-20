# List Page Views with ShinyStat

Retrieves page view report data from ShinyStat.

## Endpoint

- **Method:** `POST`
- **Path:** `/ajax`
- **Base URL:** `https://report.shinystat.com`
- **Official documentation:** [List Page Views](https://www.shinystat.com/it/guida-elemento_report-accessi-pagine-viste.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `href` | body | `string` | yes | Temporary default route for this report. Replace with the exact internal ShinyStat report route once authenticated dashboard evidence is available. |
