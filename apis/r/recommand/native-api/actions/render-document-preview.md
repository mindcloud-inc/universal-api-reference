# Render Document Preview with Recommand

Retrieves a rendered preview for a Recommand document.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/documents/:documentId/render/:type`
- **Base URL:** `https://app.recommand.eu`
- **Official documentation:** [Render Document Preview](https://recommand.eu/en/reference/documents/render-document-preview)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `documentId` | path | `string` | yes | documentId parameter. |
| `type` | path | `string` | yes | type parameter. |
