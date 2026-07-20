# Create Memory Document Upload URL with Langbase

## Endpoint

- **Method:** `POST`
- **Path:** `v1/memory/documents`
- **Base URL:** `https://api.langbase.com`
- **Official documentation:** [Create Memory Document Upload URL](https://langbase.com/docs/api-reference/memory/document-upload)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `memoryName` | body | `string` | yes | Target memory name for the document upload URL. |
| `fileName` | body | `string` | no | Original file name that Langbase should prepare the upload URL for. |
