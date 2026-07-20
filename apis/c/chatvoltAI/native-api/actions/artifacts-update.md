# Update Artifact with Chatvolt AI

Updates an artifact in Chatvolt AI.

## Endpoint

- **Method:** `PUT`
- **Path:** `/artifacts/{id}`
- **Base URL:** `https://api.chatvolt.ai`
- **Official documentation:** [Update Artifact](https://docs.chatvolt.ai/api-reference/endpoint/artifacts/update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | — |
| `name` | body | `string` | no | Name for application/json requests. |
| `description` | body | `string` | no | Description for application/json requests. |
| `price` | body | `number` | no | Price for application/json requests. |
| `externalUrl` | body | `string` | no | ExternalUrl for application/json requests. |
| `customJson` | body | `object` | no | CustomJson for application/json requests. |
| `categoryId` | body | `string` | no | CategoryId for application/json requests. |
| `isActive` | body | `boolean` | no | IsActive for application/json requests. |
