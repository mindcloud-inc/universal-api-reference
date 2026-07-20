# Create document from XML with PrexView

Creates a document in PrexView from XML data.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/transform`
- **Base URL:** `https://api.prexview.com`
- **Official documentation:** [Create document from XML](https://prexview.com/docs/api/)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `xml` | body | `string` | yes | XML data to transform into the selected output format. |
| `template` | body | `string` | yes | PrexView template name to use for document creation. |
| `output` | body | `list<string>` | yes | Document format to create: html, pdf, png, or jpg. Accepted values: `HTML`, `JPG`, `PDF`, `PNG`. |
| `templateBackup` | body | `string` | no | Backup template name to use when the main template is unavailable. |
| `note` | body | `string` | no | Optional metadata note for the transaction, up to 500 characters. Maximum length: 500. |
