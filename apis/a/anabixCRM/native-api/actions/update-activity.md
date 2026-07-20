# Update Activity with Anabix CRM

Updates an existing activity in Anabix CRM.

## Endpoint

- **Method:** `POST`
- **Path:** `/api`
- **Base URL:** `https://app.anabix.cz`
- **Official documentation:** [Update Activity](https://www.anabix.cz/wp-content/uploads/2025/02/anabix_api_manual-2025.pdf)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `idActivity` | body | `number` | yes | — |
| `body` | body | `string` | no | Updated activity body from Anabix activity data. |
