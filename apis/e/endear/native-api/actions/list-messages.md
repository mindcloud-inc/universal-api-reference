# List Messages with Endear

## Endpoint

- **Method:** `POST`
- **Path:** `/graphql`
- **Base URL:** `https://api.endearhq.com`
- **Official documentation:** [List Messages](https://docs.endearhq.com/docs/introduction)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `variables.first` | body | `number` | no | First for the Endear GraphQL operation. |
| `variables.after` | body | `string` | no | After for the Endear GraphQL operation. |
| `variables.sortBy` | body | `string` | no | Sort By for the Endear GraphQL operation. |
| `variables.sortDir` | body | `string` | no | Sort Dir for the Endear GraphQL operation. |
| `variables.conversationId` | body | `string` | yes | Conversation Id for the Endear GraphQL operation. |
