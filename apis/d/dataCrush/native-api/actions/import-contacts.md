# Search Contacts By Email with DataCrush

Finds contacts in DataCrush by email address.

## Endpoint

- **Method:** `POST`
- **Path:** `/contact/search`
- **Base URL:** `https://api.datacrush.la`
- **Official documentation:** [Search Contacts By Email](https://help.datacrush.la/hc/es-419/articles/360048047972--API-REST-v1-Contactos-Manejo-y-b%C3%BAsqueda-de-contactos-con-la-API-de-DataCrush)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | yes | Email address to search for. |
