# Create Customer with Endear

## Endpoint

- **Method:** `POST`
- **Path:** `/graphql`
- **Base URL:** `https://api.endearhq.com`
- **Official documentation:** [Create Customer](https://docs.endearhq.com/docs/introduction)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `variables.creatorId` | body | `string` | no | Creator Id for the Endear GraphQL operation. |
| `variables.assignedTo[]` | body | `array<string>` | no | Assigned To for the Endear GraphQL operation. |
| `variables.attributes[]` | body | `array<object>` | no | Attributes for the Endear GraphQL operation. |
