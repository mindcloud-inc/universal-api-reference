# List Contacts In Contact List with Conexteo

Finds contacts in a Conexteo contact list.

## Endpoint

- **Method:** `GET`
- **Path:** `/contactlists/:id/contacts`
- **Base URL:** `https://api.conexteo.com`
- **Official documentation:** [List Contacts In Contact List](https://developers.conexteo.com/contacts-dune-liste-de-contacts-pagination-24126521e0)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Identifier of the contact list whose contacts should be listed. |
