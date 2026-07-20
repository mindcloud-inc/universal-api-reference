# List audit event details with MoySklad

Retrieves audit event details from MoySklad.

## Endpoint

- **Method:** `GET`
- **Path:** `audit/:id/events`
- **Base URL:** `https://api.moysklad.ru/api/remap/1.2`
- **Official documentation:** [List audit event details](https://dev.moysklad.ru/doc/api/remap/1.2/audit/#audit-audit)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | MoySklad audit event ID. |
