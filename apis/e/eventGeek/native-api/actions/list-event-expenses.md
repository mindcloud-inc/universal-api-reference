# List Event Expenses with EventGeek

Retrieves event expense records from EventGeek.

## Endpoint

- **Method:** `GET`
- **Path:** `/events/:event_id/expenses`
- **Base URL:** `https://app.circa.co/api/v1`
- **Official documentation:** [List Event Expenses](https://docs.circa.co/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `event_id` | path | `string` | yes | Circa event identifier. |
