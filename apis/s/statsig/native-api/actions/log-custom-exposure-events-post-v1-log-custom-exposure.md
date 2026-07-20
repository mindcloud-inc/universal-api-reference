# Log Custom Exposure Events with Statsig

Logs custom exposure events to Statsig.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/log_custom_exposure`
- **Base URL:** `https://statsigapi.net`
- **API:** rest
- **Official documentation:** [Log Custom Exposure Events](https://docs.statsig.com/api-reference/events/log-custom-exposure-events)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `exposures` | body | `list<object>` | yes | Array of exposure events to log. |
| `user` | body | `object` | no | Shared user object for all exposures. |
| `statsigMetadata` | body | `object` | no | SDK metadata for diagnostics and exposure behavior. |
