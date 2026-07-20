# Day-Wise Stats Reports with Zoho PageSense

Retrieves day-wise stats reports from Zoho PageSense.

## Endpoint

- **Method:** `POST`
- **Path:** `/portal/:portalName/fulltrackingreports`
- **Base URL:** `https://pagesense.zoho.com/pagesense/rest/v1`
- **Official documentation:** [Day-Wise Stats Reports](https://www.zoho.com/pagesense/developerguide/apidocs/daywisestatsreport.html)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `portalName` | path | `string` | yes | Portal identifier in the path. |
| `full_tracking_reports.start_date` | body | `date` | yes | Report start date in YYYY-MM-DD format. |
| `full_tracking_reports.end_date` | body | `date` | yes | Report end date in YYYY-MM-DD format. |
| `full_tracking_reports.primary_dimension` | body | `string` | yes | Dimension to group metrics by. |
| `full_tracking_reports.metrics` | body | `list<string>` | yes | Requested metric keys. |
