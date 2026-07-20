# Create Artifact with Chatvolt AI

Creates an artifact in Chatvolt AI.

## Endpoint

- **Method:** `POST`
- **Path:** `/artifacts`
- **Base URL:** `https://api.chatvolt.ai`
- **Official documentation:** [Create Artifact](https://docs.chatvolt.ai/api-reference/endpoint/artifacts/create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Name for application/json requests. |
| `description` | body | `string` | no | Description for application/json requests. |
| `price` | body | `number` | no | Price for application/json requests. |
| `externalUrl` | body | `string` | no | ExternalUrl for application/json requests. |
| `customJson` | body | `object` | no | CustomJson for application/json requests. |
| `categoryId` | body | `string` | yes | CategoryId for application/json requests. |
| `isActive` | body | `boolean` | no | IsActive for application/json requests. |
