# Create Offline Agreement with Reepay

Creates an offline agreement in Reepay.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/agreement/offline`
- **Base URL:** `https://api.frisbii.com`
- **Official documentation:** [Create Offline Agreement](https://docs.frisbii.com/reference/createofflineagreement)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `currencies[]` | body | `array<string>` | no |
| `handle` | body | `string` | yes |
| `instructions` | body | `string` | yes |
| `name` | body | `string` | yes |
| `payment_type` | body | `string` | yes |
| `settle_type` | body | `string` | yes |
