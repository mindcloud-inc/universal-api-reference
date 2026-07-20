# Delete Contact with DataCrush

Deletes an existing contact from DataCrush.

## Endpoint

- **Method:** `POST`
- **Path:** `/contact/delete`
- **Base URL:** `https://api.datacrush.la`
- **Official documentation:** [Delete Contact](https://help.datacrush.la/hc/es-419/articles/360048047972--API-REST-v1-Contactos-Manejo-y-b%C3%BAsqueda-de-contactos-con-la-API-de-DataCrush)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contact_key` | body | `string` | yes | Identifier of the contact to delete. |
