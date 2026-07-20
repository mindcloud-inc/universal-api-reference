# Update Contact with Anabix CRM

Updates an existing contact in Anabix CRM.

## Endpoint

- **Method:** `POST`
- **Path:** `/api`
- **Base URL:** `https://app.anabix.cz`
- **Official documentation:** [Update Contact](https://www.anabix.cz/wp-content/uploads/2025/02/anabix_api_manual-2025.pdf)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `idContact` | body | `number` | yes | — |
| `email` | body | `string` | no | Updated contact email address from Anabix contact data. |
