# Create Contact with Anabix CRM

Creates a new contact in Anabix CRM.

## Endpoint

- **Method:** `POST`
- **Path:** `/api`
- **Base URL:** `https://app.anabix.cz`
- **Official documentation:** [Create Contact](https://www.anabix.cz/wp-content/uploads/2025/02/anabix_api_manual-2025.pdf)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `email` | body | `string` | yes |
| `firstName` | body | `string` | no |
| `lastName` | body | `string` | no |
