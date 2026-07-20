# List Bounce Visits with ShinyStat

Retrieves bounce visit metrics from ShinyStat.

## Endpoint

- **Method:** `POST`
- **Path:** `/ajax`
- **Base URL:** `https://report.shinystat.com`
- **Official documentation:** [List Bounce Visits](https://www.shinystat.com/it/guida-elemento_rimbalzi_report.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `href` | body | `string` | yes | Temporary default route for this report. Replace with the exact internal ShinyStat report route once authenticated dashboard evidence is available. |
