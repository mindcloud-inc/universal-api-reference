# Update Task with Anabix CRM

Updates an existing task in Anabix CRM.

## Endpoint

- **Method:** `POST`
- **Path:** `/api`
- **Base URL:** `https://app.anabix.cz`
- **Official documentation:** [Update Task](https://www.anabix.cz/wp-content/uploads/2025/02/anabix_api_manual-2025.pdf)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `idTask` | body | `number` | yes | — |
| `body` | body | `string` | no | Updated task body from Anabix task data. |
