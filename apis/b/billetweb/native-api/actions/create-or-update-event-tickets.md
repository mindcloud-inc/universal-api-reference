# Create Or Update Event Tickets with Billetweb

Creates or updates event tickets in Billetweb.

## Endpoint

- **Method:** `POST`
- **Path:** `/event/:id/tickets_update`
- **Base URL:** `https://www.billetweb.fr/api`
- **Official documentation:** [Create Or Update Event Tickets](https://www.billetweb.fr/bo/api.php#/api/event/:id/tickets_update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Event identifier whose ticket catalog will be updated. |
| `data[]` | body | `array<object>` | yes | Array of ticket objects to create or update. |
