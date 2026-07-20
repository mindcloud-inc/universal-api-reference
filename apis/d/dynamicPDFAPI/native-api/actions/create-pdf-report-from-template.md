# Create PDF Report From Template with DynamicPDF

Creates a PDF report from a template in DynamicPDF API.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1.0/dlex-layout`
- **Base URL:** `https://api.dpdf.io`
- **Official documentation:** [Create PDF Report From Template](https://dpdf.io/docs/tutorials/designer/creating-a-report-using-template)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `DlexPath` | body | `string` | yes | Cloud storage path to the DLEX template. |
| `LayoutData` | body | `file` | yes | JSON layout data file for the DLEX template. |
