# Create Schedule with Moodo & Moodo AIR

Creates a new schedule for a Moodo box.

## Endpoint

- **Method:** `POST`
- **Path:** `/schedules`
- **Base URL:** `https://rest.moodo.co/api`
- **Official documentation:** [Create Schedule](https://rest.moodo.co/#/schedules/create_schedule)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `weekdays` | body | `object` | yes | Weekday activation map. |
