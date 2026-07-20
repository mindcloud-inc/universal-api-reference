# Add Contact To Opportunity with DataCrush

Adds a contact to an opportunity in DataCrush.

## Endpoint

- **Method:** `POST`
- **Path:** `/crm/opportunity/contact-add`
- **Base URL:** `https://api.datacrush.la`
- **Official documentation:** [Add Contact To Opportunity](https://help.datacrush.la/hc/es-419/articles/360048050372-API-REST-v1-Oportunidades-Manejo-y-b%C3%BAsqueda-de-oportunidades-con-la-API-de-DataCrush)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `opportunity_key` | body | `string` | yes | Opportunity key to update. |
| `contact_key` | body | `string` | yes | Contact key to associate. |
| `role` | body | `string` | yes | Contact role in the opportunity. |
| `main` | body | `string` | yes | Whether the contact is the main contact: 1 or 0. |
