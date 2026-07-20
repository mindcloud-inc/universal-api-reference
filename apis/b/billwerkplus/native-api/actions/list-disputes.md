# List Disputes with Billwerkplus

Retrieves disputes from Billwerkplus.

## Endpoint

- **Method:** `GET`
- **Path:** `/list/dispute`
- **Base URL:** `https://api.frisbii.com/v1`
- **Official documentation:** [List Disputes](https://docs.frisbii.com/reference/getdisputelist)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `invoice` | query | `string` | no | Invoice handle filter. |
| `state[]` | query | `array<string>` | no | Dispute states to include. Multiple values are allowed. Send multiple values as a array. |
| `outcome[]` | query | `array<string>` | no | Dispute outcomes to include. Multiple values are allowed. Send multiple values as a array. |
| `reason[]` | query | `array<string>` | no | Dispute reasons to include. Multiple values are allowed. Send multiple values as a array. |
| `range` | query | `list` | no | Time attribute to limit by: created or resolved. Accepted values: `0`, `1`. |
| `transaction` | query | `string` | no | Transaction id filter. |
