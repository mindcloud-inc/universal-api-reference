# Bulk Delete Artifacts with Chatvolt AI

Deletes artifacts from Chatvolt AI.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/artifacts`
- **Base URL:** `https://api.chatvolt.ai`
- **Official documentation:** [Bulk Delete Artifacts](https://docs.chatvolt.ai/api-reference/endpoint/artifacts/bulk-delete)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ids[]` | body | `array<string>` | yes | Ids for application/json requests. |
