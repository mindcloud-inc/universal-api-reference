# Update Contact List with Conexteo

Updates an existing contact list in Conexteo.

## Endpoint

- **Method:** `PUT`
- **Path:** `/contactlists/:id`
- **Base URL:** `https://api.conexteo.com`
- **Official documentation:** [Update Contact List](https://developers.conexteo.com/mise-%C3%A0-jour-dune-liste-de-contacts-24126518e0)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Conexteo contact-list identifier. |
| `name` | body | `string` | no | Updated name for the contact list. |
