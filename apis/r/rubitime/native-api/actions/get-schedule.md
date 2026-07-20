# Get Schedule with Rubitime

Retrieves booking dates and times from Rubitime.

## Endpoint

- **Method:** `POST`
- **Path:** `/get-schedule`
- **Base URL:** `https://rubitime.ru/api2`
- **Official documentation:** [Get Schedule](https://rubitime.ru/faq/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `branch_id` | body | `number` | yes | Rubitime branch ID. |
| `cooperator_id` | body | `number` | yes | Rubitime employee/cooperator ID. |
| `service_id` | body | `number` | yes | Rubitime service ID. |
| `only_available` | body | `number` | no | Use 1 to return only available slots or 0 to return only occupied slots. Omit to return all slots. |
