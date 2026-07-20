# Update Category with Chatvolt AI

Updates a category in Chatvolt AI.

## Endpoint

- **Method:** `PUT`
- **Path:** `/artifact-categories/{id}`
- **Base URL:** `https://api.chatvolt.ai`
- **Official documentation:** [Update Category](https://docs.chatvolt.ai/api-reference/endpoint/artifacts/categories/update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | — |
| `name` | body | `string` | no | Name for application/json requests. |
| `description` | body | `string` | no | Description for application/json requests. |
| `parentId` | body | `string` | no | ParentId for application/json requests. |
| `isActive` | body | `boolean` | no | IsActive for application/json requests. |
