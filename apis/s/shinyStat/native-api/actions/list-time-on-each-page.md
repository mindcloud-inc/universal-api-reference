# List Time On Each Page with ShinyStat

Retrieves time on page metrics for each page from ShinyStat.

## Endpoint

- **Method:** `POST`
- **Path:** `/ajax`
- **Base URL:** `https://report.shinystat.com`
- **Official documentation:** [List Time On Each Page](https://www.shinystat.com/it/guida-elemento_report-tempi-permanenza-media-ogni-pagina.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `href` | body | `string` | yes | Temporary default route for this report. Replace with the exact internal ShinyStat report route once authenticated dashboard evidence is available. |
