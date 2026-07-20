# List Charges with Billwerkplus

Retrieves charges from Billwerkplus.

## Endpoint

- **Method:** `GET`
- **Path:** `/list/charge`
- **Base URL:** `https://api.frisbii.com/v1`
- **Official documentation:** [List Charges](https://docs.frisbii.com/reference/getchargelist)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `handle` | query | `string` | no | Exact charge handle. |
| `customer` | query | `string` | no | Customer handle filter. |
| `state[]` | query | `array<string>` | no | Charge states to include. Multiple values are allowed. Send multiple values as a array. |
| `currency[]` | query | `array<string>` | no | Charge currency filter. Multiple values are allowed. Send multiple values as a array. |
| `range` | query | `list` | no | Time attribute to limit by: created or settled. Accepted values: `0`, `1`. |
