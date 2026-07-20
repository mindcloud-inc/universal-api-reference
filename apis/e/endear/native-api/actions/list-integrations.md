# List Integrations with Endear

## Endpoint

- **Method:** `POST`
- **Path:** `/graphql`
- **Base URL:** `https://api.endearhq.com`
- **Official documentation:** [List Integrations](https://docs.endearhq.com/docs/introduction)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `variables.first` | body | `number` | no | First for the Endear GraphQL operation. |
| `variables.after` | body | `string` | no | After for the Endear GraphQL operation. |
| `variables.sortBy` | body | `string` | no | Sort By for the Endear GraphQL operation. |
| `variables.sortDir` | body | `string` | no | Sort Dir for the Endear GraphQL operation. |
| `variables.search` | body | `string` | no | Search for the Endear GraphQL operation. |
| `variables.includeDisabled` | body | `boolean` | yes | Include Disabled for the Endear GraphQL operation. |
| `variables.type` | body | `string` | no | Type for the Endear GraphQL operation. |
