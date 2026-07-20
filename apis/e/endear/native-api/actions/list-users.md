# List Users with Endear

## Endpoint

- **Method:** `POST`
- **Path:** `/graphql`
- **Base URL:** `https://api.endearhq.com`
- **Official documentation:** [List Users](https://docs.endearhq.com/docs/introduction)

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
| `variables.byStatus` | body | `string` | no | By Status for the Endear GraphQL operation. |
| `variables.type` | body | `string` | no | Type for the Endear GraphQL operation. |
| `variables.memberOfTeamIds[]` | body | `array<string>` | no | Member Of Team Ids for the Endear GraphQL operation. |
| `variables.byAvailability` | body | `string` | no | By Availability for the Endear GraphQL operation. |
| `variables.hasProfilePicture` | body | `boolean` | no | Has Profile Picture for the Endear GraphQL operation. |
