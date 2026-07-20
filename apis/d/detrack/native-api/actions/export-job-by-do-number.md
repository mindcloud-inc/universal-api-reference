# Export Job By D.O. Number with Detrack

Exports a job document from Detrack by D.O. number.

## Endpoint

- **Method:** `GET`
- **Path:** `/dn/jobs/export/:do_number`
- **Base URL:** `https://app.detrack.com/api/v2`
- **Official documentation:** [Export Job By D.O. Number](https://detrackapiv2.docs.apiary.io/#reference/jobs/export-by-do/download-exported-file)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `do_number` | path | `string` | yes | D.O. number of the job to export. |
| `document` | query | `string` | no | Document type to export, such as pod or shipping-label. |
| `format` | query | `string` | no | Export format, such as pdf or tiff. |
