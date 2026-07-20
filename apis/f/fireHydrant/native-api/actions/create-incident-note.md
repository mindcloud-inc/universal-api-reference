# Create Incident Note with FireHydrant

Creates a new incident note in FireHydrant.

## Endpoint

- **Method:** `POST`
- **Path:** `/incidents/:incident_id/notes`
- **Base URL:** `https://api.firehydrant.io/v1`
- **Official documentation:** [Create Incident Note](https://docs.firehydrant.com/reference/create_incident_note)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `body` | body | `string` | yes | The incident note body. |
| `incident_id` | path | `string` | yes | The FireHydrant incident ID. |
| `occurred_at` | body | `date` | no | ISO8601 timestamp for when the note occurred. |
| `visibility` | body | `list` | no | Who can see the note. Accepted values: `0`, `1`, `2`. |
