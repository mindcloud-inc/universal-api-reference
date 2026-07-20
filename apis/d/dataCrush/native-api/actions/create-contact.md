# Create Contact with DataCrush

Creates a new contact in DataCrush.

## Endpoint

- **Method:** `POST`
- **Path:** `/contact/insert`
- **Base URL:** `https://api.datacrush.la`
- **Official documentation:** [Create Contact](https://help.datacrush.la/hc/es-419/articles/360048047972--API-REST-v1-Contactos-Manejo-y-b%C3%BAsqueda-de-contactos-con-la-API-de-DataCrush)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | yes | Email address for the new contact. |
| `first_name` | body | `string` | no | First name for the contact. |
| `last_name` | body | `string` | no | Last name for the contact. |
