# Create Event with EventGeek

Creates a new event in EventGeek.

## Endpoint

- **Method:** `POST`
- **Path:** `/events`
- **Base URL:** `https://app.circa.co/api/v1`
- **Official documentation:** [Create Event](https://docs.circa.co/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Event name. |
| `status` | body | `string` | yes | Event status. |
| `team_id` | body | `string` | yes | Team that owns the event. |
