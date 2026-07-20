# Process a Bank Statement asynchronously with Veryfi

Creates a new bank statement asynchronously in Veryfi.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v8/partner/bank-statements/async`
- **Base URL:** `https://api.veryfi.com`
- **Official documentation:** [Process a Bank Statement asynchronously](https://docs.veryfi.com/api/bank-statements/process-a-bank-statement-asynchronously/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `meta.external_id` | body | `string` | no | Possible values: non-empty External ID you want to associate with the document. |
| `external_id` | body | `string` | no | Possible values: non-empty A custom identification value. Use this if you would like to assign your own ID to documents. This parameter is useful when mapping this document to a service or resource outside Veryfi. |
| `meta.tags[]` | body | `array<string>` | no | Possible values: non-empty Default value: `` Tags you want to associate with the document. |
| `max_pages_to_process` | body | `number` | no | Possible values: >= 1 and <= 50 Default value: 50 Limit processing to number of pages. |
| `categories[]` | body | `array<string>` | no | Default value: `` A list of custom categories for transaction categorization. If provided, these categories will be used instead of the user's default categories. |
| `package_path` | body | `string` | no | Possible values: non-empty A path to a file in an S3 bucket, e.g. 'some/receipt.jpg |
| `bucket` | body | `string` | no | Possible values: non-empty An S3 bucket for 'package_path', e.g. 'documents'. |
| `file_data` | body | `string` | no | Possible values: non-empty Used to upload a document via base64 encoded string, could be raw or data URI scheme . This is the least effective way to upload a document for processing. See file_urls or uploading zip files . |
| `file_url` | body | `string` | no | Possible values: non-empty A URL to a publicly accessible document to be sent to Veryfi for processing. |
| `file_urls[]` | body | `array<string>` | no | Possible values: non-empty An array of URLs to publicly accessible documents to be sent to Veryfi for processing. |
| `file_name` | body | `string` | no | Possible values: non-empty An optional filename. Useful to determine file type. |
| `auto_delete` | body | `boolean` | no | Default value: false Whether to delete the document after processing. In async deletes the document after the first GET request. |
| `file` | body | `string` | no | A binary file. Submitting zipped documents through this parameter is the fastest way to process any document. |
