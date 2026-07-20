# Convert a Document to Markdown with Veryfi

Creates a new markdown document in Veryfi.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v8/partner/document-to-markdown`
- **Base URL:** `https://api.veryfi.com`
- **Official documentation:** [Convert a Document to Markdown](https://docs.veryfi.com/api/document-to-markdown/convert-a-document-to-markdown/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `external_id` | body | `string` | no | External reference ID for tracking. |
| `package_path` | body | `string` | no | Possible values: non-empty A path to a file in an S3 bucket, e.g. 'some/receipt.jpg |
| `bucket` | body | `string` | no | Possible values: non-empty An S3 bucket for 'package_path', e.g. 'documents'. |
| `file_data` | body | `string` | no | Possible values: non-empty Used to upload a document via base64 encoded string, could be raw or data URI scheme . This is the least effective way to upload a document for processing. See file_urls or uploading zip files . |
| `file_url` | body | `string` | no | Possible values: non-empty A URL to a publicly accessible document to be sent to Veryfi for processing. |
| `file_urls[]` | body | `array<string>` | no | Possible values: non-empty An array of URLs to publicly accessible documents to be sent to Veryfi for processing. |
| `file_name` | body | `string` | no | Possible values: non-empty An optional filename. Useful to determine file type. |
| `details` | body | `boolean` | no | A field used to determine whether or not to return bounding boxes along with markdown. |
| `document_type` | body | `string` | no | Default value: document Type of document being converted (e.g., 'receipt', 'invoice', 'contract'). |
| `tags[]` | body | `array<string>` | no | Tags to attach to the document. |
| `max_pages_to_process` | body | `number` | no | Possible values: >= 1 and <= 50 Default value: 50 Limit processing to number of pages. |
| `file` | body | `string` | no | A binary file. Submitting zipped documents through this parameter is the fastest way to process any document. |
