# Split PDF with PDF Tools by Tachytelic

## Endpoint

- **Method:** `POST`
- **Path:** `/split`
- **Base URL:** `https://pdf.tachytelic.net/api`
- **Official documentation:** [Split PDF](https://learn.microsoft.com/en-us/connectors/pdftoolsbytachytelic/#split-pdf)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `PdfFileContent` | body | `string` | yes | Base64-encoded PDF file content. |
| `SplitType` | body | `list` | yes | How to split the PDF: NumberOfPages or SpecifiedRanges. Accepted values: `0`, `1`. |
| `PagesPerSplit` | body | `number` | no | Number of pages per output file when Split Type is NumberOfPages. |
| `PageRanges` | body | `string` | no | Page ranges to split by when Split Type is SpecifiedRanges, for example 1-2,4. |
