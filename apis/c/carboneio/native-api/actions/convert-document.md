# Convert Document with Carbone.io

Creates a converted document from uploaded templates in Carbone.io.

## Endpoint

- **Method:** `POST`
- **Path:** `/render/template`
- **Base URL:** `https://api.carbone.io`
- **Official documentation:** [Convert Document](https://carbone.io/documentation/developer/http-api/generate-reports.html#generate-a-report)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `batchOutput` | body | `string` | no | Output format for batch processing, such as zip or pdf. |
| `batchReportName` | body | `string` | no | File name template for each item produced by batch rendering. |
| `batchSplitBy` | body | `string` | no | JSON path used to split an array into multiple generated reports. |
| `complement` | body | `object` | no | Additional JSON data exposed in the template as complement fields. |
| `converter` | body | `string` | no | Optional conversion engine override when Carbone exposes multiple converters. |
| `convertTo` | body | `string` | no | Target format name such as pdf, docx, xlsx, html, csv, png, or webp. |
| `currencyRates` | body | `object` | no | Custom currency rates object used for conversion. |
| `currencySource` | body | `string` | no | Source currency code used when Carbone performs currency conversion. |
| `currencyTarget` | body | `string` | no | Target currency code used when Carbone performs currency conversion. |
| `data` | body | `object` | yes | JSON dataset merged into the template. |
| `enum` | body | `object` | no | Enumeration map available to Carbone enum conversion helpers. |
| `hardRefresh` | body | `boolean` | no | Recompute pagination and table of contents after rendering. |
| `lang` | body | `string` | no | Language code used for locale-aware formatting. |
| `reportName` | body | `string` | no | Output file name template for the generated report. |
| `template` | body | `string` | yes | Base64-encoded contents of the source document to convert. |
| `timezone` | body | `string` | no | IANA timezone used when rendering date and time formatters. |
| `translations` | body | `object` | no | Localization dictionary used by translation tags in the template. |
| `variableStr` | body | `string` | no | Additional variable string passed to the render engine. |
