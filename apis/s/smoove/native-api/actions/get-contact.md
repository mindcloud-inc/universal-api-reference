# Get Contact with Smoove

Retrieves a contact from Smoove by identifier.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/Contacts/:id`
- **Base URL:** `https://rest.smoove.io`
- **Official documentation:** [Get Contact](https://rest.smoove.io)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | — |
| `by` | query | `list` | no | Accepted values: `CellPhone`, `ContactId`, `Email`, `ExternalId`. |
| `fields` | query | `string` | no | — |
| `includeCustomFields` | query | `boolean` | no | — |
| `includeLinkedLists` | query | `boolean` | no | — |
