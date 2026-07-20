# Create Export with Voucherify

Creates a new export in Voucherify.

## Endpoint

- **Method:** `POST`
- **Path:** `/exports`
- **Base URL:** `https://us1.api.voucherify.io/v1`
- **Official documentation:** [Create Export](https://docs.voucherify.io/api-reference/exports)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `exported_object` | body | `string` | yes | — |
| `parameters.fields[]` | body | `array<string>` | no | Send multiple values as a array. |
