# Create Personal Room with LiveWebinar

Creates a personal room in LiveWebinar.

## Endpoint

- **Method:** `POST`
- **Path:** `api/widgets/:widget_id/personal`
- **Base URL:** `https://api.archiebot.com`
- **Official documentation:** [Create Personal Room](https://docs.archiebot.com/?version=latest#739a2b58-c457-4d88-8ec0-94589f2e5180)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | yes | — |
| `firstname` | body | `string` | no | — |
| `lastname` | body | `string` | no | — |
| `role` | body | `string` | no | — |
| `type` | body | `string` | no | — |
| `widget_id` | path | `string` | yes | — |
| `widget_id` | path | `string` | yes | Widget identifier |
| `email` | body | `string` | yes | Recipient email |
