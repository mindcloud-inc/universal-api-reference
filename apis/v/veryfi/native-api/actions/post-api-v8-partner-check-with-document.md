# Process a Check With Remittance with Veryfi

Creates a new check with remittance in Veryfi.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v8/partner/check-with-document`
- **Base URL:** `https://api.veryfi.com`
- **Official documentation:** [Process a Check With Remittance](https://docs.veryfi.com/api/checks/process-a-check-with-remittance/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `bounding_boxes` | body | `boolean` | no | A field used to determine whether or not to return bounding_box and bounding_region for extracted fields in the Document response. |
| `confidence_details` | body | `boolean` | no | A field used to determine whether or not to return the score and ocr_score fields in the Document response. |
| `external_id` | body | `string` | no | Possible values: non-empty A custom identification value. Use this if you would like to assign your own ID to documents. This parameter is useful when mapping this document to a service or resource outside Veryfi. |
| `meta.tags[]` | body | `array<string>` | no | Possible values: non-empty Default value: `` Tags you want to associate with the document. |
| `package_path` | body | `string` | no | Possible values: non-empty A path to a file in an S3 bucket, e.g. 'some/receipt.jpg |
| `bucket` | body | `string` | no | Possible values: non-empty An S3 bucket for 'package_path', e.g. 'documents'. |
| `file_data` | body | `string` | no | Possible values: non-empty Used to upload a document via base64 encoded string, could be raw or data URI scheme . This is the least effective way to upload a document for processing. See file_urls or uploading zip files . |
| `file_url` | body | `string` | no | Possible values: non-empty A URL to a publicly accessible document to be sent to Veryfi for processing. |
| `file_urls[]` | body | `array<string>` | no | Possible values: non-empty An array of URLs to publicly accessible documents to be sent to Veryfi for processing. |
| `file_name` | body | `string` | no | Possible values: non-empty An optional filename. Useful to determine file type. |
| `meta.external_id` | body | `string` | no | Possible values: non-empty External ID you want to associate with the document. |
| `file` | body | `string` | no | A binary file. Submitting zipped documents through this parameter is the fastest way to process any document. |
