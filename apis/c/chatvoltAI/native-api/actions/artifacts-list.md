# List Artifacts with Chatvolt AI

Retrieves artifacts from Chatvolt AI.

## Endpoint

- **Method:** `GET`
- **Path:** `/artifacts`
- **Base URL:** `https://api.chatvolt.ai`
- **Official documentation:** [List Artifacts](https://docs.chatvolt.ai/api-reference/endpoint/artifacts/list)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `categoryId` | query | `string` | no | Filter by category ID. |
| `name` | query | `string` | no | Filter by exact name match. |
| `search` | query | `string` | no | General search string (name, description, id). |
