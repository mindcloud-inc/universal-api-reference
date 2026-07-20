# Search Contacts In List with DataCrush

Finds contacts in DataCrush by list ID.

## Endpoint

- **Method:** `POST`
- **Path:** `/contact/search`
- **Base URL:** `https://api.datacrush.la`
- **Official documentation:** [Search Contacts In List](https://help.datacrush.la/hc/es-419/articles/360048047972--API-REST-v1-Contactos-Manejo-y-b%C3%BAsqueda-de-contactos-con-la-API-de-DataCrush)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `list_id` | body | `string` | yes | List identifier to filter contacts. |
