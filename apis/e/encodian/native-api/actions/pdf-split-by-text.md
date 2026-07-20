# PDF Split By Text with Encodian

Splits a PDF by text in Encodian.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/PDF/SplitPdfByText`
- **Base URL:** `https://api.apps-encodian.com`
- **Official documentation:** [PDF Split By Text](https://support.encodian.com/hc/en-gb/articles/360012726397)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Filename` | body | `string` | yes | The filename of the source PDF document including the file extension. |
| `FileContent` | body | `string` | yes | A Base64 encoded representation of the source PDF document. |
| `SplitValue` | body | `string` | yes | Specify either a text value or a regular expression. |
| `IsExpression` | body | `boolean` | yes | Set whether to evaluate the split value as a string or regular expression. |
| `PrefixFilename` | body | `boolean` | yes | Set whether the expression value should be used within the output filename. |
| `SplitPdfByTextType` | body | `string` | yes | Select whether to split on the first instance, last instance, or all instances matching the split value. |
| `SplitAction` | body | `string` | yes | Select whether to split on, before, after, or remove the page containing the split value. |
