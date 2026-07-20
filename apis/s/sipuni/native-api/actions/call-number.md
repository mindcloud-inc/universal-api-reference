# Call Number with Sipuni

## Endpoint

- **Method:** `POST`
- **Path:** `/callback/call_number`
- **Base URL:** `https://sipuni.com/api`
- **Official documentation:** [Call Number](https://doc.sipuni.com/articles/636-640--otpravka-sobytij-http/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `phone` | query | `string` | yes | External customer phone number to call. |
| `sipnumber` | query | `string` | yes | Sipuni employee short extension that initiates or receives the callback order. |
| `reverse` | query | `string` | no | Sipuni callback mode flag. Default 0 follows the standard employee-to-customer callback order. |
| `antiaon` | query | `string` | no | Caller ID hiding flag. Default 0 leaves caller ID behavior unchanged. |
