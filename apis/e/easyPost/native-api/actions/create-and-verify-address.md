# Create And Verify Address with EasyPost

Creates and verifies a new address in EasyPost.

## Endpoint

- **Method:** `POST`
- **Path:** `/addresses/create_and_verify`
- **Base URL:** `https://api.easypost.com/v2`
- **Official documentation:** [Create And Verify Address](https://docs.easypost.com/docs/addresses)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `address` | body | `object` | yes | Address object to create and verify. |
| `verify[]` | body | `array<string>` | no | Optional verification types to request, such as delivery. |
