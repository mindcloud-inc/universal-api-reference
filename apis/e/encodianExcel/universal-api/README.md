# <img src="https://images.mindcloud.co/apps/icons/encodian_1777473716979.jpeg" alt="Encodian - Excel logo" width="28" height="28"> Encodian - Excel: Universal API

Encodian Flowr Excel connector for creating, merging, securing, parsing, and manipulating Microsoft Excel and CSV files through Encodian's document automation API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/encodianExcel/latest
- **Actions:** 19
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.encodian.com/product/flowr/
- **Vendor API docs:** https://learn.microsoft.com/en-gb/connectors/encodianexcel/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [CSV - Parse](actions/csv-parse.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/encodianExcel/latest/actions/csv-parse?connectionId=$CONNECTION_ID&fileContent=bmFtZSxhbW91bnQKQWxpY2UsMTAKQm9iLDIwCg%3D%3D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (19)

### Csv

| Action | Method | Description |
| --- | --- | --- |
| [CSV - Parse](actions/csv-parse.md) | GET | Parses a CSV file into JSON in Encodian - Excel. |

### Excel

| Action | Method | Description |
| --- | --- | --- |
| [Excel - Add Rows](actions/add-rows-to-excel.md) | PUT | Adds rows to an Excel file in Encodian - Excel. |
| [Excel - Delete Worksheets](actions/delete-excel-worksheets.md) | DELETE | Deletes worksheets from an Excel file in Encodian - Excel. |
| [Excel - Delete Rows](actions/delete-rows-from-excel.md) | DELETE | Deletes rows from an Excel file in Encodian - Excel. |
| [Excel - Add Image Header or Footer](actions/excel-add-image-header-or-footer.md) | PUT | Adds an image header or footer to an Excel file in Encodian - Excel. |
| [Excel - Add Text Header or Footer](actions/excel-add-text-headers-and-footers.md) | PUT | Adds a text header or footer to an Excel file in Encodian - Excel. |
| [Excel - Remove Headers and Footers](actions/excel-remove-headers-and-footers.md) | DELETE | Removes headers and footers from an Excel file in Encodian - Excel. |
| [Excel - Replace Text](actions/excel-replace-text.md) | PUT | Finds and replaces text in an Excel file in Encodian - Excel. |
| [Excel - Separate Worksheets](actions/excel-separate-worksheets.md) | PUT | Separates worksheets into individual files in Encodian - Excel. |
| [Excel - Add Text Watermark](actions/excel-watermark-text.md) | PUT | Adds a text watermark to an Excel file in Encodian - Excel. |
| [Excel - Remove Text Watermark](actions/excel-watermark-text-remove.md) | DELETE | Removes text watermarks from an Excel file in Encodian - Excel. |
| [Excel - Extract Worksheets](actions/extract-excel-worksheets.md) | GET | Extracts worksheets from an Excel file in Encodian - Excel. |
| [Excel - Extract Rows](actions/get-rows-from-excel.md) | GET | Retrieves rows from an Excel file in Encodian - Excel. |
| [Excel - Merge Files](actions/merge-array-of-excel-documents.md) | PUT | Merges Excel files into one file in Encodian - Excel. |
| [Excel - Merge Rows](actions/merge-excel-rows.md) | PUT | Merges rows from Excel files into one worksheet in Encodian - Excel. |
| [Excel - Populate](actions/populate-excel.md) | PUT | Populates an Excel workbook with JSON data in Encodian - Excel. |
| [Excel - Secure](actions/secure-excel.md) | PUT | Secures and protects an Excel file in Encodian - Excel. |
| [Excel - Unlock](actions/unlock-excel.md) | DELETE | Unlocks an Excel file in Encodian - Excel. |
| [Excel - Update Rows](actions/update-rows-in-excel.md) | PUT | Updates rows in an Excel file in Encodian - Excel. |

