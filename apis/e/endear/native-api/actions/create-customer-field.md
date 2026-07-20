# Create Customer Field with Endear

## Endpoint

- **Method:** `POST`
- **Path:** `/graphql`
- **Base URL:** `https://api.endearhq.com`
- **Official documentation:** [Create Customer Field](https://docs.endearhq.com/docs/introduction)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `variables.key` | body | `string` | yes | Key for the Endear GraphQL operation. |
| `variables.label` | body | `string` | yes | Label for the Endear GraphQL operation. |
| `variables.description` | body | `string` | no | Description for the Endear GraphQL operation. |
| `variables.type` | body | `string` | yes | Type for the Endear GraphQL operation. |
| `variables.allowMultiple` | body | `boolean` | yes | Allow Multiple for the Endear GraphQL operation. |
| `variables.isUserEditable` | body | `boolean` | yes | Is User Editable for the Endear GraphQL operation. |
| `variables.order` | body | `string` | no | Order for the Endear GraphQL operation. |
| `variables.options[]` | body | `array<object>` | no | Options for the Endear GraphQL operation. |
| `variables.currency` | body | `string` | no | Currency for the Endear GraphQL operation. |
| `variables.customerFieldGroupId` | body | `string` | no | Customer Field Group Id for the Endear GraphQL operation. |
