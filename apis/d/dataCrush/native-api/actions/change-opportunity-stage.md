# Change Opportunity Stage with DataCrush

Updates an opportunity stage in DataCrush.

## Endpoint

- **Method:** `POST`
- **Path:** `/crm/opportunity/stage`
- **Base URL:** `https://api.datacrush.la`
- **Official documentation:** [Change Opportunity Stage](https://help.datacrush.la/hc/es-419/articles/360048050372-API-REST-v1-Oportunidades-Manejo-y-b%C3%BAsqueda-de-oportunidades-con-la-API-de-DataCrush)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `opportunity_key` | body | `string` | yes | Opportunity key to update. |
| `stage` | body | `string` | yes | New stage value. |
