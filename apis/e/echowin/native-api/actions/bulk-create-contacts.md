# Bulk Create Contacts with echowin

Creates contacts in echowin in bulk.

## Endpoint

- **Method:** `POST`
- **Path:** `/contacts/bulk`
- **Base URL:** `https://echo.win/api/v1`
- **Official documentation:** [Bulk Create Contacts](https://echo.win/api-docs/contacts#bulk-create)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `contacts[]` | body | `array<object>` | yes |
