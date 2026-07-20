# Create Tracker with Ship24

Creates a new tracker in Ship24.

## Endpoint

- **Method:** `POST`
- **Path:** `/public/v1/trackers`
- **Base URL:** `https://api.ship24.com`
- **Official documentation:** [Create Tracker](https://docs.ship24.com/tracking-api-reference/#/operations/create-tracker)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `trackingNumber` | body | `string` | yes | Tracking number of the shipment. |
| `clientTrackerId` | body | `string` | no | Your unique identifier for this shipment. |
| `shipmentReference` | body | `string` | no | Your reference for this shipment. |
| `originCountryCode` | body | `string` | no | Sender country code. |
| `destinationCountryCode` | body | `string` | no | Recipient country code. Recommended to improve tracking accuracy. |
| `destinationPostCode` | body | `string` | no | Recipient postal or ZIP code. Recommended to improve tracking accuracy. |
| `shippingDate` | body | `date` | no | Shipment date. Keep it close to the real ship date to improve matching accuracy. |
| `courierCode[]` | body | `array<string>` | no | Up to 3 courier codes handling the shipment. Recommended to improve tracking accuracy. |
| `courierName` | body | `string` | no | Courier name or service name. |
| `orderNumber` | body | `string` | no | Order number when the shipment comes from an ecommerce order. |
| `title` | body | `string` | no | — |
| `trackingUrl` | body | `string` | no | — |
| `recipient.name` | body | `string` | no | — |
| `recipient.email` | body | `string` | no | — |
| `settings.restrictTrackingToCourierCode` | body | `boolean` | no | If true, Ship24 only tracks the courier codes you provide. |
