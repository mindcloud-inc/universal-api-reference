# Identify Bulk Contacts with SendX

## Endpoint

- **Method:** `POST`
- **Path:** `/contact/identify/bulk`
- **Base URL:** `https://api.sendx.io/api/v1/rest`
- **Official documentation:** [Identify Bulk Contacts](https://docs.sendx.io/api-reference/getting-started/identify-contact-bulk)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `contacts[]` | body | `array<object>` | yes |
