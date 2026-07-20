# Manage Contact Lists with Anabix CRM

Updates contact list memberships in Anabix CRM.

## Endpoint

- **Method:** `POST`
- **Path:** `/api`
- **Base URL:** `https://app.anabix.cz`
- **Official documentation:** [Manage Contact Lists](https://www.anabix.cz/wp-content/uploads/2025/02/anabix_api_manual-2025.pdf)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `idContact` | body | `number` | yes |
| `addTo[]` | body | `array<number>` | no |
| `removeFrom[]` | body | `array<number>` | no |
