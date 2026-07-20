# List Page Views Per Visit with ShinyStat

Retrieves page views per visit from ShinyStat.

## Endpoint

- **Method:** `POST`
- **Path:** `/ajax`
- **Base URL:** `https://report.shinystat.com`
- **Official documentation:** [List Page Views Per Visit](https://www.shinystat.com/it/guida-elemento_report-pagine-pagine-viste-per-visita.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `href` | body | `string` | yes | Temporary default route for this report. Replace with the exact internal ShinyStat report route once authenticated dashboard evidence is available. |
