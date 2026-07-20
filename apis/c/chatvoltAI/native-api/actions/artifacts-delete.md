# Delete/Toggle Artifact with Chatvolt AI

Deletes an artifact from Chatvolt AI, or toggles its active status.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/artifacts/{id}`
- **Base URL:** `https://api.chatvolt.ai`
- **Official documentation:** [Delete/Toggle Artifact](https://docs.chatvolt.ai/api-reference/endpoint/artifacts/delete)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | — |
| `action` | query | `string` | no | Action to perform: "delete" to remove, "toggle" to switch active status. |
