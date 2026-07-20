# Process a Contract with Veryfi

Creates a new contract in Veryfi.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v8/partner/contracts`
- **Base URL:** `https://api.veryfi.com`
- **Official documentation:** [Process a Contract](https://docs.veryfi.com/api/contracts/process-a-contract/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `max_pages_to_process` | body | `number` | no | Possible values: >= 1 and <= 50 Default value: 50 Limit processing to number of pages. A page is a pdf page or an image |
| `auto_delete` | body | `boolean` | no | Default value: false Delete this contract from Veryfi after data has been extracted |
| `file_data` | body | `string` | no | Possible values: non-empty The least effective way to submit files. Base64 encoded string, could be raw or datauri https://en.wikipedia.org/wiki/Data_URI_scheme E.g. 'data:application/zip;base64,iVBORw0KGgoAAAANSUhEUgAAAAEAAAABCAQAAAC1HAwCAAAAC0lEQVQYV2NgYAAAAAMAAWgmWQ0AAAAASUVORK5CYII=' |
| `file_url` | body | `string` | no | Possible values: non-empty |
| `package_path` | body | `string` | no | Possible values: non-empty A path to file in S3 bucket, e.g. 'some/contract.pdf |
| `bucket` | body | `string` | no | Possible values: non-empty An S3 bucket for 'package_path', e.g. 'contracts' |
| `file_name` | body | `string` | no | Possible values: non-empty Optional filename, helps to determine file type |
| `meta.external_id` | body | `string` | no | Possible values: non-empty External ID you want to associate with the document. |
| `meta.tags[]` | body | `array<string>` | no | Possible values: non-empty Default value: `` Tags you want to associate with the document. |
| `external_id` | body | `string` | no | Possible values: non-empty A custom identification value. Use this if you would like to assign your own ID to documents. This parameter is useful when mapping this document to a service or resource outside Veryfi. |
| `file_urls[]` | body | `array<string>` | no | Possible values: non-empty An array of URLs to publicly accessible documents to be sent to Veryfi for processing. |
| `file` | body | `string` | no | A binary file. Submitting zipped documents through this parameter is the fastest way to process any document. |
