# Update Doc with Dovetail

Updates an existing doc in Dovetail.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v1/docs/:docId`
- **Base URL:** `https://dovetail.com/api`
- **Official documentation:** [Update Doc](https://developers.dovetail.com/reference/patch_v1-docs-docid)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `docId` | path | `string` | yes | — |
| `title` | body | `string` | no | Doc title. |
