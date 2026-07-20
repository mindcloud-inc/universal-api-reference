# Log Custom Events with Statsig

Logs custom events to Statsig.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/log_event`
- **Base URL:** `https://statsigapi.net`
- **API:** rest
- **Official documentation:** [Log Custom Events](https://docs.statsig.com/api-reference/events/log-custom-events)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `events` | body | `list<object>` | yes | Array of events to log. |
| `user` | body | `object` | no | Shared user object for all events; individual events may override it. |
| `statsigMetadata` | body | `object` | no | SDK metadata for diagnostics and exposure behavior. |
