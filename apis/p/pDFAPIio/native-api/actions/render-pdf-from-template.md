# Render PDF from Template with PDF-API.io

Creates a PDF document from a template in PDF-API.io.

## Endpoint

- **Method:** `POST`
- **Path:** `/templates/:templateId/pdf`
- **Base URL:** `https://pdf-api.io/api`
- **Official documentation:** [Render PDF from Template](https://pdf-api.io/en/docs/api/render-pdf)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `templateId` | path | `list<number>` | yes | The identifier of the template to use for generating the PDF. |
| `data` | body | `object` | yes | Key-value pairs representing the data to replace in the template. |
| `output` | body | `list<string>` | no | Optional output format for the generated PDF response. Accepted values: `pdf`, `url`. |
