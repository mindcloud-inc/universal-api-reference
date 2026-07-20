# Search Contacts By Contact Key with DataCrush

Finds contacts in DataCrush by contact key.

## Endpoint

- **Method:** `POST`
- **Path:** `/contact/search`
- **Base URL:** `https://api.datacrush.la`
- **Official documentation:** [Search Contacts By Contact Key](https://help.datacrush.la/hc/es-419/articles/360048047972--API-REST-v1-Contactos-Manejo-y-b%C3%BAsqueda-de-contactos-con-la-API-de-DataCrush)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contact_key` | body | `string` | yes | Unique contact key to search for. |
