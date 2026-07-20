# List Monthly Unique Visitors with ShinyStat

Retrieves monthly unique visitor metrics from ShinyStat.

## Endpoint

- **Method:** `POST`
- **Path:** `/ajax`
- **Base URL:** `https://report.shinystat.com`
- **Official documentation:** [List Monthly Unique Visitors](https://www.shinystat.com/it/guida-elemento_report-accessi-visitatori-unici-mensili.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `href` | body | `string` | yes | Temporary default route for this report. Replace with the exact internal ShinyStat report route once authenticated dashboard evidence is available. |
