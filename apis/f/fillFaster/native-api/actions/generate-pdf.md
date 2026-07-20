# Generate PDF with FillFaster

Generates a filled PDF from a FillFaster form.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/generatePDF`
- **Base URL:** `https://api.fillfaster.com`
- **Official documentation:** [Generate PDF](https://documenter.getpostman.com/view/18912453/2s8ZDVZ3UJ#f726d97c-c44c-4b68-86a7-7f06bb1db8c2)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fid` | body | `string` | yes | Form template identifier. |
| `prefill_data` | body | `object` | no | Field values to render into the generated PDF. |
