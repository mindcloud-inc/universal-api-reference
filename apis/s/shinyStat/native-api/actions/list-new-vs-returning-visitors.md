# List New Vs Returning Visitors with ShinyStat

Retrieves new versus returning visitor metrics from ShinyStat.

## Endpoint

- **Method:** `POST`
- **Path:** `/ajax`
- **Base URL:** `https://report.shinystat.com`
- **Official documentation:** [List New Vs Returning Visitors](https://www.shinystat.com/it/guida-elemento_Visitatori-nuovi-e-di-ritorno.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `href` | body | `string` | yes | Temporary default route for this report. Replace with the exact internal ShinyStat report route once authenticated dashboard evidence is available. |
