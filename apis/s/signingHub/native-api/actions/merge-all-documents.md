# Merge All Documents with SigningHub

Merges all documents in a package in SigningHub.

## Endpoint

- **Method:** `POST`
- **Path:** `/v4/packages/:packageId/documents/merge`
- **Base URL:** `https://api.signinghub.com`
- **Official documentation:** [Merge All Documents](https://manuals.ascertia.com/SigningHub/10.0/Api/#tag/Document-Package/operation/V4_MergeDocument_MergeAllDocuments)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `packageId` | path | `number` | yes | The document package whose documents should be merged. |
