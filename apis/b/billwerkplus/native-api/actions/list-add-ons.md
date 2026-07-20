# List Add-Ons with Billwerkplus

Retrieves add-ons from Billwerkplus.

## Endpoint

- **Method:** `GET`
- **Path:** `/list/add_on`
- **Base URL:** `https://api.frisbii.com/v1`
- **Official documentation:** [List Add-Ons](https://docs.frisbii.com/reference/getaddonlist)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `from` | query | `date` | no | Inclusive start of the local account time range. |
| `to` | query | `date` | no | Exclusive end of the local account time range. |
| `interval` | query | `string` | no | ISO 8601 duration counted back from To. |
| `range` | query | `list` | no | Time attribute to limit by: created or deleted. Accepted values: `0`, `1`. |
| `handle` | query | `string` | no | Exact add-on handle. |
| `handle_prefix` | query | `string` | no | Add-on handle prefix. |
| `state` | query | `list` | no | Add-on state: active or deleted. Accepted values: `0`, `1`. |
| `type` | query | `list` | no | Add-on type: on_off or quantity. Accepted values: `0`, `1`. |
| `name` | query | `string` | no | Add-on name filter. |
| `plan` | query | `string` | no | Plan handle filter. |
| `currency[]` | query | `array<string>` | no | Currency filter. Multiple values are allowed. Send multiple values as a array. |
