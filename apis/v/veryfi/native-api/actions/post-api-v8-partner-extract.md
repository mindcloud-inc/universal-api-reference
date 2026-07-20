# Classify and possibly extract data from a document with Veryfi

Classifies a document and may extract data in Veryfi.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v8/partner/extract`
- **Base URL:** `https://api.veryfi.com`
- **Official documentation:** [Classify and possibly extract data from a document](https://docs.veryfi.com/api/classify-and-possibly-extract-data-from-a-document/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `external_id` | body | `string` | no | Possible values: non-empty A custom identification value. Use this if you would like to assign your own ID to documents. This parameter is useful when mapping this document to a service or resource outside Veryfi. |
| `package_path` | body | `string` | no | Possible values: non-empty A path to a file in an S3 bucket, e.g. 'some/receipt.jpg |
| `bucket` | body | `string` | no | Possible values: non-empty An S3 bucket for 'package_path', e.g. 'documents'. |
| `file_data` | body | `string` | no | Possible values: non-empty Used to upload a document via base64 encoded string, could be raw or data URI scheme . This is the least effective way to upload a document for processing. See file_urls or uploading zip files . |
| `file_url` | body | `string` | no | Possible values: non-empty A URL to a publicly accessible document to be sent to Veryfi for processing. |
| `file_urls[]` | body | `array<string>` | no | Possible values: non-empty An array of URLs to publicly accessible documents to be sent to Veryfi for processing. |
| `file_name` | body | `string` | no | Possible values: non-empty An optional filename. Useful to determine file type. |
| `document_types[]` | body | `array<object>` | yes | Possible values: >= 1 The types to classify the document into. If not a preset type, it must be a valid blueprint name. string string |
| `file` | body | `string` | no | A binary file. Submitting zipped documents through this parameter is the fastest way to process any document. |
