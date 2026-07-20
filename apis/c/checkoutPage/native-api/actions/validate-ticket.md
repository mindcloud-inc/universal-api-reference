# Validate Ticket with Checkout Page

Validates a ticket in Checkout Page by QR code.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/tickets/validate/:qrCode`
- **Base URL:** `https://api.checkoutpage.com`
- **Official documentation:** [Validate Ticket](https://checkoutpage.com/docs/api/v1/tickets/validate)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `qrCode` | path | `string` | yes | Validate ticket |
| `metadata[]` | body | `array<object>` | no | — |
