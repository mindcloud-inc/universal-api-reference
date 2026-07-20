# Unassign Label from Document with Recommand

Removes a label from a Recommand document.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/api/v1/documents/:documentId/labels/:labelId`
- **Base URL:** `https://app.recommand.eu`
- **Official documentation:** [Unassign Label from Document](https://recommand.eu/en/reference/documents/unassign-label-from-document)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `documentId` | path | `string` | yes | documentId parameter. |
| `labelId` | path | `string` | yes | labelId parameter. |
