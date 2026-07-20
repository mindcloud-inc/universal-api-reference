# Read Document with Dynalist

Retrieves a document from Dynalist.

## Endpoint

- **Method:** `POST`
- **Path:** `/doc/read`
- **Base URL:** `https://dynalist.io/api/v1/`
- **Official documentation:** [Read Document](https://apidocs.dynalist.io/#get-content-of-a-document)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file_id` | body | `string` | yes | ID of the document to read. |
