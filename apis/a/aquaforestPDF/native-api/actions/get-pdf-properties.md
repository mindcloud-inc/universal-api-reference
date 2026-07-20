# Get PDF properties with Aquaforest PDF

Retrieves PDF file properties from Aquaforest PDF.

## Endpoint

- **Method:** `POST`
- **Path:** `/GetPDFInfo`
- **Base URL:** `https://aquaforest-pdf.azure-api.net/AquaforestPDFAPIV2`
- **Official documentation:** [Get PDF properties](https://learn.microsoft.com/en-us/connectors/aquaforest/#get-pdf-properties)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fileContent` | body | `file` | yes | The content of the source PDF file. |
| `pageLimit` | body | `number` | no | Maximum number of pages to process when checking hidden text or searchability. |
