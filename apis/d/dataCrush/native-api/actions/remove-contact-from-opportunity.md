# Remove Contact From Opportunity with DataCrush

Removes a contact from an opportunity in DataCrush.

## Endpoint

- **Method:** `POST`
- **Path:** `/crm/opportunity/contact-delete`
- **Base URL:** `https://api.datacrush.la`
- **Official documentation:** [Remove Contact From Opportunity](https://help.datacrush.la/hc/es-419/articles/360048050372-API-REST-v1-Oportunidades-Manejo-y-b%C3%BAsqueda-de-oportunidades-con-la-API-de-DataCrush)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `opportunity_key` | body | `string` | yes | Opportunity key to update. |
| `contact_key` | body | `string` | yes | Contact key to remove. |
