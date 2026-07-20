# List Audit Events with Pachca (Admin)

Retrieves audit events from the Pachca Admin API.

## Endpoint

- **Method:** `GET`
- **Path:** `/audit_events`
- **Base URL:** `https://api.pachca.com/api/shared/v1`
- **Official documentation:** [List Audit Events](https://dev.pachca.com/api/security/list)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `actor_id` | query | `number` | no | Filter by actor id. |
| `actor_type` | query | `string` | no | Filter by actor type. |
| `entity_id` | query | `number` | no | Filter by entity id. |
| `entity_type` | query | `string` | no | Filter by entity type. |
| `start_time` | query | `date` | no | — |
| `end_time` | query | `date` | no | — |
| `event_key` | query | `string` | no | — |
| `limit` | query | `number` | no | — |
| `cursor` | query | `string` | no | — |
