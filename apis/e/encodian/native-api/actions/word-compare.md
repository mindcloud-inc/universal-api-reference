# Word Compare with Encodian

Compares Word or PDF documents in Encodian.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/Word/CompareWordDocuments`
- **Base URL:** `https://api.apps-encodian.com`
- **Official documentation:** [Word Compare](https://support.encodian.com/hc/en-gb/articles/360018576278-Compare-Word-Documents)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `FileContentOne` | body | `string` | yes | A Base64 encoded representation of the first file to compare. |
| `FileContentTwo` | body | `string` | yes | A Base64 encoded representation of the second file to compare. |
| `Author` | body | `string` | no | Set the author name used to denote differences in the output document. |
| `IgnoreFormatting` | body | `boolean` | no | Specifies whether to ignore document formatting differences. |
| `CaseInsensitive` | body | `boolean` | no | Specifies whether to compare differences in documents as case insensitive. |
| `IgnoreComments` | body | `boolean` | no | Specifies whether to compare differences in comments. |
| `IgnoreTables` | body | `boolean` | no | Specifies whether to compare differences in table data. |
| `IgnoreFields` | body | `boolean` | no | Specifies whether to compare differences in fields. |
| `IgnoreFootnotes` | body | `boolean` | no | Specifies whether to compare differences in footnotes and endnotes. |
| `IgnoreTextboxes` | body | `boolean` | no | Specifies whether to compare differences in text boxes. |
| `IgnoreHeadersAndFooters` | body | `boolean` | no | Specifies whether to compare differences in headers and footers. |
