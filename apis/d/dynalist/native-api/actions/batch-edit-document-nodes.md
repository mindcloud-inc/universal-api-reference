# Batch Edit Document Nodes with Dynalist

Updates multiple document nodes in Dynalist.

## Endpoint

- **Method:** `POST`
- **Path:** `/doc/edit`
- **Base URL:** `https://dynalist.io/api/v1/`
- **Official documentation:** [Batch Edit Document Nodes](https://apidocs.dynalist.io/#make-change-to-the-content-of-a-document)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file_id` | body | `string` | yes | ID of the document to edit. |
| `changes[]` | body | `array<object>` | yes | Array of documented node-level changes to apply. |
