# Update Tracker with Ship24

Updates an existing tracker in Ship24.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/public/v1/trackers/:trackerId`
- **Base URL:** `https://api.ship24.com`
- **Official documentation:** [Update Tracker](https://docs.ship24.com/tracking-api-reference/#/operations/update-tracker-by-trackerId)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `trackerId` | path | `string` | yes | Ship24 tracker ID returned when the tracker was created. |
| `isSubscribed` | body | `boolean` | no | Set false to stop future tracking updates and webhook notifications. |
| `courierCode` | body | `string` | no | Courier code that handles the shipment. Ship24 allows up to 3 codes. |
| `originCountryCode` | body | `string` | no | Sender country code in ISO alpha-2 or alpha-3 format. |
| `destinationCountryCode` | body | `string` | no | Recipient country code in ISO alpha-2 or alpha-3 format. |
| `destinationPostCode` | body | `string` | no | Recipient postal code or ZIP code. |
| `shippingDate` | body | `date` | no | Shipment date in an ISO-compatible date or datetime format. |
