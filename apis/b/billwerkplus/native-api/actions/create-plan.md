# Create Plan with Billwerkplus

Creates a plan in Billwerkplus.

## Endpoint

- **Method:** `POST`
- **Path:** `/plan`
- **Base URL:** `https://api.frisbii.com/v1`
- **Official documentation:** [Create Plan](https://docs.frisbii.com/reference/createplanjson)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Plan name. |
| `handle` | body | `string` | yes | Unique plan handle. |
| `amount` | body | `number` | yes | Plan amount in the smallest account currency unit. |
| `schedule_type` | body | `string` | yes | Plan scheduling type. |
| `interval_length` | body | `number` | yes | Number of schedule units between renewals. |
| `amount_incl_vat` | body | `boolean` | no | Whether amount includes VAT. |
