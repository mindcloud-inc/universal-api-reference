# Export Data Points with Simple Analytics

Exports raw data points from Simple Analytics in JSON.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/export/datapoints`
- **Base URL:** `https://simpleanalytics.com`
- **Official documentation:** [Export Data Points](https://docs.simpleanalytics.com/api/export-data-points)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `hostname` | query | `string` | yes | Website hostname to export data for, for example `simpleanalytics.com`. |
| `start` | query | `string` | yes | Start date in `YYYY-MM-DD` or `YYYY-MM-DDTHH` format. |
| `end` | query | `string` | yes | End date in `YYYY-MM-DD` or `YYYY-MM-DDTHH` format. |
| `fields` | query | `string` | yes | Comma-separated raw data fields to return, such as `added_iso,path`. |
| `type` | query | `string` | yes | Export data type, for example `pageviews`. |
| `timezone` | query | `string` | no | IANA time zone such as `Europe/Amsterdam`. |
| `robots` | query | `boolean` | no | Whether to include robot traffic in the export. |
