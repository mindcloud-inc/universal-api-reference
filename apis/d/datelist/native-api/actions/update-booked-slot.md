# Update Booked Slot with Datelist

Updates an existing booked slot in Datelist.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/booked_slots/:id`
- **Base URL:** `https://datelist.io/api`
- **Official documentation:** [Update Booked Slot](https://apidoc.datelist.io/booked_slots)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | The ID of the booked slot to update. |
| `body` | body | `object` | no | Booked slot fields to update, using the documented booked-slot object shape. |
