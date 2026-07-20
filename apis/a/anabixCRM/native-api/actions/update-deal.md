# Update Deal with Anabix CRM

Updates an existing deal in Anabix CRM.

## Endpoint

- **Method:** `POST`
- **Path:** `/api`
- **Base URL:** `https://app.anabix.cz`
- **Official documentation:** [Update Deal](https://www.anabix.cz/wp-content/uploads/2025/02/anabix_api_manual-2025.pdf)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `idDeal` | body | `number` | yes | — |
| `body` | body | `string` | no | Updated deal description from Anabix deal data. |
