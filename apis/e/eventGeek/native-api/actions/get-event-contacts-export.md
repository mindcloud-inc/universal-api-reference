# Get Event Contacts Export with EventGeek

Retrieves an event contacts export from EventGeek.

## Endpoint

- **Method:** `GET`
- **Path:** `/events/:event_id/contacts/exports/:export_id`
- **Base URL:** `https://app.circa.co/api/v1`
- **Official documentation:** [Get Event Contacts Export](https://docs.circa.co/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `event_id` | path | `string` | yes | Circa event identifier. |
| `export_id` | path | `string` | yes | Circa export identifier. |
