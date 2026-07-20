# List Checklists with Checkvist

Retrieves checklists from Checkvist.

## Endpoint

- **Method:** `GET`
- **Path:** `/checklists.json`
- **Base URL:** `https://checkvist.com`
- **Official documentation:** [List Checklists](https://checkvist.com/auth/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `archived` | query | `boolean` | no | Return archived checklists. |
| `order` | query | `string` | no | Sort checklists, for example updated_at:asc or id:desc. |
| `skip_stats` | query | `boolean` | no | Skip checklist user and task stats for a faster response. |
