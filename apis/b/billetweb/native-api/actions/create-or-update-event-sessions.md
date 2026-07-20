# Create Or Update Event Sessions with Billetweb

Creates or updates event sessions in Billetweb.

## Endpoint

- **Method:** `POST`
- **Path:** `/event/:id/dates_update`
- **Base URL:** `https://www.billetweb.fr/api`
- **Official documentation:** [Create Or Update Event Sessions](https://www.billetweb.fr/bo/api.php#/api/event/:id/dates_update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Event identifier whose sessions will be updated. |
| `data[]` | body | `array<object>` | yes | Array of session objects to create or update. |
