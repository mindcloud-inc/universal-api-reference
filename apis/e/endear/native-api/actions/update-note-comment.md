# Update Note Comment with Endear

## Endpoint

- **Method:** `POST`
- **Path:** `/graphql`
- **Base URL:** `https://api.endearhq.com`
- **Official documentation:** [Update Note Comment](https://docs.endearhq.com/docs/introduction)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `variables.id` | body | `string` | yes | Id for the Endear GraphQL operation. |
| `variables.comment` | body | `string` | yes | Comment for the Endear GraphQL operation. |
| `variables.updaterId` | body | `string` | yes | Updater Id for the Endear GraphQL operation. |
