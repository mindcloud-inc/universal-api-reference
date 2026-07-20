# Update Opportunity with DataCrush

Updates an existing opportunity in DataCrush.

## Endpoint

- **Method:** `POST`
- **Path:** `/crm/opportunity/update`
- **Base URL:** `https://api.datacrush.la`
- **Official documentation:** [Update Opportunity](https://help.datacrush.la/hc/es-419/articles/360048050372-API-REST-v1-Oportunidades-Manejo-y-b%C3%BAsqueda-de-oportunidades-con-la-API-de-DataCrush)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `opportunity_key` | body | `string` | yes | Opportunity key to update. |
| `name` | body | `string` | no | Updated opportunity name. |
| `close_date` | body | `string` | no | Updated close date in YYYY-MM-DD format. |
| `amount` | body | `number` | no | Updated opportunity amount. |
| `account_key` | body | `string` | no | Updated account key. |
