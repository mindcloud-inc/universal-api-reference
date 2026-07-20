# List Weekly Unique Visitors with ShinyStat

Retrieves weekly unique visitor metrics from ShinyStat.

## Endpoint

- **Method:** `POST`
- **Path:** `/ajax`
- **Base URL:** `https://report.shinystat.com`
- **Official documentation:** [List Weekly Unique Visitors](https://www.shinystat.com/it/guida-elemento_visitatori-browser-unici-settimanali.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `href` | body | `string` | yes | Temporary default route for this report. Replace with the exact internal ShinyStat report route once authenticated dashboard evidence is available. |
