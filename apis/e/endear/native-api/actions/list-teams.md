# List Teams with Endear

## Endpoint

- **Method:** `POST`
- **Path:** `/graphql`
- **Base URL:** `https://api.endearhq.com`
- **Official documentation:** [List Teams](https://docs.endearhq.com/docs/introduction)

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
| `variables.accessibleToUserId` | body | `string` | no | Accessible To User Id for the Endear GraphQL operation. |
| `variables.teamMemberIds[]` | body | `array<string>` | no | Team Member Ids for the Endear GraphQL operation. |
| `variables.byStatus` | body | `string` | no | By Status for the Endear GraphQL operation. |
