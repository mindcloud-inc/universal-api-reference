# Get Process Timeline with NileDesk

Retrieves a process or board item timeline in NileDesk.

## Endpoint

- **Method:** `POST`
- **Path:** `/GetProcessTimeline`
- **Base URL:** `https://app.niledesk.com/api/public`
- **Official documentation:** [Get Process Timeline](https://niledesk.com/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `process_id` | body | `string` | yes | The NileDesk process or board item whose timeline should be returned. |
