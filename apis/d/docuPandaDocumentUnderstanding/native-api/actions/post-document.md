# Submit a Document for Processing with DocuPanda - Document Understanding

Creates a document processing request in DocuPanda.

## Endpoint

- **Method:** `POST`
- **Path:** `/document`
- **Base URL:** `https://app.docupipe.ai`
- **Official documentation:** [Submit a Document for Processing](https://docs.docupipe.ai/reference/post_document)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `document` | body | `object` | yes | — |
| `pages` | body | `list<number>` | no | List of page numbers to be parsed (zero indexed). If not provided, all pages will be parsed. |
| `pages[]` | body | `array<number>` | no | List of page numbers to be parsed (zero indexed). If not provided, all pages will be parsed. |
| `dataset` | body | `string` | no | Name of the dataset to which you want to assign this document. It can be any string. This is useful to group your documents |
| `metadata` | body | `object` | no | Optional metadata to associate with the document. |
| `parseVersion` | body | `number` | no | Version of parsing. Available versions are 1, 2, 3 |
| `processingMethod` | body | `string` | no | — |
| `timeout` | body | `number` | no | The timeout in seconds for the job for webhook error reporting |
| `workflowId` | body | `string` | no | *Advanced Feature* Unique identifier of the workflow to be applied to the doucment once it is processed. See `POST /workflow/onSubmitDocument` for more details. |
