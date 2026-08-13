# Batch Upsert Contacts with HubSpot

## Endpoint

- **Method:** `POST`
- **Path:** `crm/objects/2026-03/contacts/batch/upsert`
- **Base URL:** `https://api.hubapi.com`
- **API:** REST - Query Pagination
- **Official documentation:** [Batch Upsert Contacts](https://developers.hubspot.com/docs/api-reference/latest/crm/objects/contacts/batch/upsert-contacts)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `inputs[]` | body | `array<object>` | yes | Up to 100 contact upsert objects. Each item requires id, idProperty, and properties; properties accepts HubSpot contact property names and values. |
