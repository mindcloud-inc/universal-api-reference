# Update Contact with DataCrush

Updates an existing contact in DataCrush.

## Endpoint

- **Method:** `POST`
- **Path:** `/contact/update`
- **Base URL:** `https://api.datacrush.la`
- **Official documentation:** [Update Contact](https://help.datacrush.la/hc/es-419/articles/360048047972--API-REST-v1-Contactos-Manejo-y-b%C3%BAsqueda-de-contactos-con-la-API-de-DataCrush)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contact_key` | body | `string` | yes | Identifier of the contact to update. |
| `email` | body | `string` | no | New email for the contact. |
| `first_name` | body | `string` | no | Updated first name. |
| `last_name` | body | `string` | no | Updated last name. |
