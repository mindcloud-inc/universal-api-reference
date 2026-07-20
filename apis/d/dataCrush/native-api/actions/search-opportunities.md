# Search Opportunities with DataCrush

Finds opportunities in DataCrush by name.

## Endpoint

- **Method:** `POST`
- **Path:** `/crm/opportunity/search`
- **Base URL:** `https://api.datacrush.la`
- **Official documentation:** [Search Opportunities](https://help.datacrush.la/hc/es-419/articles/360048050372-API-REST-v1-Oportunidades-Manejo-y-b%C3%BAsqueda-de-oportunidades-con-la-API-de-DataCrush)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Opportunity name to search for. |
