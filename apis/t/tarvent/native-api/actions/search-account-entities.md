# Search Account Entities with Tarvent

Finds account entities in Tarvent by search text.

## Endpoint

- **Method:** `POST`
- **Path:** `/graphql`
- **Base URL:** `https://api.tarvent.com`
- **Official documentation:** [Search Account Entities](https://developer.tarvent.com/queries/allAccountEntities)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `variables.searchValue` | body | `string` | yes | The text to search across account entities. |
