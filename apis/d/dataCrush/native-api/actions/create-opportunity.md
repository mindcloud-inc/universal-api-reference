# Create Opportunity with DataCrush

Creates a new opportunity in DataCrush.

## Endpoint

- **Method:** `POST`
- **Path:** `/crm/opportunity/insert`
- **Base URL:** `https://api.datacrush.la`
- **Official documentation:** [Create Opportunity](https://help.datacrush.la/hc/es-419/articles/360048050372-API-REST-v1-Oportunidades-Manejo-y-b%C3%BAsqueda-de-oportunidades-con-la-API-de-DataCrush)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Opportunity name. |
| `close_date` | body | `string` | yes | Close date in YYYY-MM-DD format. |
| `amount` | body | `number` | yes | Opportunity amount. |
| `account_key` | body | `string` | yes | Account key linked to the opportunity. |
| `stage` | body | `string` | yes | Initial opportunity stage. |
