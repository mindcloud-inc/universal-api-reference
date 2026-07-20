# Create Note with Endear

## Endpoint

- **Method:** `POST`
- **Path:** `/graphql`
- **Base URL:** `https://api.endearhq.com`
- **Official documentation:** [Create Note](https://docs.endearhq.com/docs/introduction)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `variables.localId` | body | `string` | no | Local Id for the Endear GraphQL operation. |
| `variables.creatorId` | body | `string` | no | Creator Id for the Endear GraphQL operation. |
| `variables.createdInTeamId` | body | `string` | no | Created In Team Id for the Endear GraphQL operation. |
| `variables.customerId` | body | `string` | no | Customer Id for the Endear GraphQL operation. |
| `variables.title` | body | `string` | no | Title for the Endear GraphQL operation. |
| `variables.description` | body | `string` | no | Description for the Endear GraphQL operation. |
| `variables.tags[]` | body | `array<string>` | no | Tags for the Endear GraphQL operation. |
| `variables.timeZone` | body | `string` | no | Time Zone for the Endear GraphQL operation. |
