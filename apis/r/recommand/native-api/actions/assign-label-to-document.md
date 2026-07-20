# Assign Label to Document with Recommand

Assigns a label to a Recommand document.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/documents/:documentId/labels/:labelId`
- **Base URL:** `https://app.recommand.eu`
- **Official documentation:** [Assign Label to Document](https://recommand.eu/en/reference/documents/assign-label-to-document)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `documentId` | path | `string` | yes | documentId parameter. |
| `labelId` | path | `string` | yes | labelId parameter. |
