# Create Ticket Timer with Syncro

Creates a ticket timer entry in Syncro.

## Endpoint

- **Method:** `POST`
- **Path:** `/tickets/:id/timer_entry`
- **Base URL:** `https://mindcloud.syncromsp.com/api/v1`
- **Official documentation:** [Create Ticket Timer](https://api-docs.syncromsp.com/#/Ticket/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | The Syncro ticket ID. |
| `start_at` | body | `date` | no | — |
| `end_at` | body | `date` | no | — |
| `duration_minutes` | body | `number` | no | — |
| `user_id` | body | `number` | no | — |
| `notes` | body | `string` | no | — |
| `product_id` | body | `number` | no | — |
