# Generate PDF From DLEX Layout with DynamicPDF

Generates a PDF from a DLEX layout in DynamicPDF API.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1.0/dlex-layout`
- **Base URL:** `https://api.dpdf.io`
- **Official documentation:** [Generate PDF From DLEX Layout](https://dpdf.io/docs/usersguide/cloud-api/cloud-api-dlex-layout)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `LayoutData` | body | `file` | yes | JSON layout data file for the DLEX report. |
| `Resource` | body | `file` | yes | DLEX resource file for the report layout. |
