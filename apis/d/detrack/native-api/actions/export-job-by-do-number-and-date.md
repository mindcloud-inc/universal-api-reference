# Export Job By D.O. Number And Date with Detrack

Exports a job document from Detrack by D.O. number and date.

## Endpoint

- **Method:** `GET`
- **Path:** `/dn/jobs/export/:do_number/:date`
- **Base URL:** `https://app.detrack.com/api/v2`
- **Official documentation:** [Export Job By D.O. Number And Date](https://detrackapiv2.docs.apiary.io/#reference/jobs/export-by-do-and-date/download-exported-file)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `do_number` | path | `string` | yes | D.O. number of the job to export. |
| `date` | path | `string` | yes | Job date in YYYY-MM-DD format. |
| `document` | query | `string` | no | Document type to export, such as pod or shipping-label. |
| `format` | query | `string` | no | Export format, such as pdf or tiff. |
