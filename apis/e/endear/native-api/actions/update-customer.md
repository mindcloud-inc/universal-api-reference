# Update Customer with Endear

## Endpoint

- **Method:** `POST`
- **Path:** `/graphql`
- **Base URL:** `https://api.endearhq.com`
- **Official documentation:** [Update Customer](https://docs.endearhq.com/docs/introduction)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `variables.editorId` | body | `string` | no | Editor Id for the Endear GraphQL operation. |
| `variables.id` | body | `string` | yes | Id for the Endear GraphQL operation. |
| `variables.archived` | body | `boolean` | yes | Archived for the Endear GraphQL operation. |
