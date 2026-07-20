# Create Comparison with Draftable

Creates a document comparison in Draftable.

## Endpoint

- **Method:** `POST`
- **Path:** `/comparisons`
- **Base URL:** `https://api.draftable.com/v1`
- **Official documentation:** [Create Comparison](https://api.draftable.com/reference/creating-comparisons)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `left.file` | body | `file` | no | Upload the left file, or provide Left Source URL instead. |
| `left.source_url` | body | `string` | no | Source URL for the left file, or upload Left File instead. |
| `left.file_type` | body | `string` | yes | File type of the left file. Accepted values: `csv`, `doc`, `docm`, `docx`, `odt`, `pdf`, `ppt`, `pptm`, `pptx`, `rtf`, `txt`, `xls`, `xlsm`, `xlsx`. |
| `left.display_name` | body | `string` | no | Display name for the left file. |
| `right.file` | body | `file` | no | Upload the right file, or provide Right Source URL instead. |
| `right.source_url` | body | `string` | no | Source URL for the right file, or upload Right File instead. |
| `right.file_type` | body | `string` | yes | File type of the right file. Accepted values: `csv`, `doc`, `docm`, `docx`, `odt`, `pdf`, `ppt`, `pptm`, `pptx`, `rtf`, `txt`, `xls`, `xlsm`, `xlsx`. |
| `right.display_name` | body | `string` | no | Display name for the right file. |
| `public` | body | `boolean` | no | Whether the comparison can be viewed without viewer URL signing. |
| `expiry_time` | body | `date` | no | When the comparison should be automatically deleted. |
| `identifier` | body | `string` | no | Optional custom identifier for the comparison. |
