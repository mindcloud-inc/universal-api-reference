# Validate Document Type with Docutray

## Endpoint

- **Method:** `POST`
- **Path:** `api/document-types/:id/validate`
- **Base URL:** `https://app.docutray.com`
- **Official documentation:** [Validate Document Type](https://docs.docutray.com/docs/operations/document-types)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Document type ID |
| `document` | body | `object` | yes | JSON document to validate |
