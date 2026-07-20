# Update Tree with Woztell

Updates a tree in your Woztell workspace.

## Endpoint

- **Method:** `POST`
- **Path:** `/`
- **Base URL:** `https://open.api.woztell.com/v3`
- **Official documentation:** [Update Tree](https://doc.woztell.com/open-api-reference/#mutation-updateTree)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `variables.input.treeId` | body | `string` | yes | Raw Woztell tree _id to update. |
| `variables.input.etag` | body | `string` | yes | Current Woztell tree etag for optimistic concurrency. |
| `variables.input.description` | body | `string` | no | Updated tree description. |
