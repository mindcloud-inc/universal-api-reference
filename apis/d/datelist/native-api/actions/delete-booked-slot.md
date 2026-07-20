# Delete Booked Slot with Datelist

Cancels an existing booked slot in Datelist.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/booked_slots/:id`
- **Base URL:** `https://datelist.io/api`
- **Official documentation:** [Delete Booked Slot](https://apidoc.datelist.io/booked_slots)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | The ID of the booked slot to delete. |
| `send_email_on_delete` | query | `boolean` | no | Whether Datelist should send an email when the booked slot is deleted. |
