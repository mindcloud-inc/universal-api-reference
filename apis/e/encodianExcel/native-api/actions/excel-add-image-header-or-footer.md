# Excel - Add Image Header or Footer with Encodian - Excel

Adds an image header or footer to an Excel file in Encodian - Excel.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/Excel/ExcelAddImageHeaderOrFooter`
- **Base URL:** `https://api.apps-encodian.com`
- **Official documentation:** [Excel - Add Image Header or Footer](https://support.encodian.com/hc/en-gb/articles/14909213525404)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fileContent` | body | `file` | yes | — |
| `imageFileContent` | body | `file` | yes | — |
| `position` | body | `list<string>` | yes | Accepted values: `FooterCentral`, `FooterLeft`, `FooterRight`, `HeaderCentral`, `HeaderLeft`, `HeaderRight`. |
