# Bulk Create Contacts with SWELLEnterprise

Creates multiple contacts in SWELLEnterprise.

## Endpoint

- **Method:** `POST`
- **Path:** `/crm/contacts/bulk`
- **Base URL:** `https://dashboard.swellsystem.com/api/v1`
- **Official documentation:** [Bulk Create Contacts](https://dashboard.swellsystem.com/docs#crm-contacts-POSTapi-v1-crm-contacts-bulk)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contacts[]` | body | `array<object>` | yes | Array of contact objects to create. |
