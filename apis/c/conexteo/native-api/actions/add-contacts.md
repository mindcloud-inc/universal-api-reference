# Add Contacts with Conexteo

Creates contacts in Conexteo.

## Endpoint

- **Method:** `POST`
- **Path:** `/contacts`
- **Base URL:** `https://api.conexteo.com`
- **Official documentation:** [Add Contacts](https://developers.conexteo.com/ajouter-undes-contacts-24126523e0)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contactlist_id` | body | `number` | yes | Identifier of the contact list that will receive the contacts. |
| `contacts[]` | body | `array<object>` | yes | Contacts to create in the target contact list. |
