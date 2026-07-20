# Get data from PDF with Aquaforest PDF

Retrieves key-value data from PDFs in Aquaforest PDF.

## Endpoint

- **Method:** `POST`
- **Path:** `/GetPageData`
- **Base URL:** `https://aquaforest-pdf.azure-api.net/AquaforestPDFAPIV2`
- **Official documentation:** [Get data from PDF](https://learn.microsoft.com/en-us/connectors/aquaforest/#get-data-from-pdf)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fileContent` | body | `file` | yes | The content of the PDF file to extract data from. |
| `expectedKeys` | body | `string` | no | One key name per line to make values available to later actions without parsing JSON. |
| `pageRange` | body | `string` | no | Page numbers to process, for example 1,3-4. |
| `pageLimit` | body | `number` | no | Maximum number of pages to process. |
| `confidenceScore` | body | `number` | no | Filter out values below this confidence score. Aquaforest recommends starting from 0.5. |
| `dateAsISO` | body | `string` | no | Date conversion format to return. |
| `stripCurrencySymbol` | body | `boolean` | no | Remove currency symbols and strings before currency values are returned. |
| `synonym` | body | `boolean` | no | Return keys that are synonyms of the expected key. |
| `trimSymbols` | body | `boolean` | no | Remove leading and trailing symbols from keys before matching. |
