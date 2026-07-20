# Create Note Comment with Endear

## Endpoint

- **Method:** `POST`
- **Path:** `/graphql`
- **Base URL:** `https://api.endearhq.com`
- **Official documentation:** [Create Note Comment](https://docs.endearhq.com/docs/introduction)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `variables.noteId` | body | `string` | yes | Note Id for the Endear GraphQL operation. |
| `variables.comment` | body | `string` | yes | Comment for the Endear GraphQL operation. |
| `variables.creatorId` | body | `string` | yes | Creator Id for the Endear GraphQL operation. |
