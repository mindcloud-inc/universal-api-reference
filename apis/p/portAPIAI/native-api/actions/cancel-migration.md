# Cancel Migration with Port API AI

Cancels a migration in Port.

## Endpoint

- **Method:** `POST`
- **Path:** `/migrations/:migration_id/cancel`
- **Base URL:** `https://api.port.io/v1`
- **Official documentation:** [Cancel Migration](https://docs.port.io/api-reference/cancel-a-migration)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `migration_id` | path | `string` | yes | The Port migration identifier. |
