# Update Note with Endear

## Endpoint

- **Method:** `POST`
- **Path:** `/graphql`
- **Base URL:** `https://api.endearhq.com`
- **Official documentation:** [Update Note](https://docs.endearhq.com/docs/introduction)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `variables.id` | body | `string` | yes | Id for the Endear GraphQL operation. |
| `variables.editorId` | body | `string` | no | Editor Id for the Endear GraphQL operation. |
| `variables.title` | body | `string` | no | Title for the Endear GraphQL operation. |
| `variables.description` | body | `string` | no | Description for the Endear GraphQL operation. |
| `variables.tags[]` | body | `array<string>` | no | Tags for the Endear GraphQL operation. |
| `variables.customerId` | body | `string` | no | Customer Id for the Endear GraphQL operation. |
