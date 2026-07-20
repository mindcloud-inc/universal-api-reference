# List Contacts In List with Smoove

Retrieves contacts from a specific Smoove list.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/Lists/:id/Contacts`
- **Base URL:** `https://rest.smoove.io`
- **Official documentation:** [List Contacts In List](https://rest.smoove.io)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string` | yes |
| `fields` | query | `string` | no |
| `includeCustomFields` | query | `boolean` | no |
| `includeLinkedLists` | query | `boolean` | no |
| `includeListAssociationTime` | query | `boolean` | no |
