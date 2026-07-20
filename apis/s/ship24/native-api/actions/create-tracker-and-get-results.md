# Create Tracker And Get Results with Ship24

Creates a tracker and retrieves tracking results in Ship24.

## Endpoint

- **Method:** `POST`
- **Path:** `/public/v1/trackers/track`
- **Base URL:** `https://api.ship24.com`
- **Official documentation:** [Create Tracker And Get Results](https://docs.ship24.com/tracking-api-reference/#/operations/create-tracker-and-get-tracking-results)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `trackingNumber` | body | `string` | yes |
| `clientTrackerId` | body | `string` | no |
| `shipmentReference` | body | `string` | no |
| `originCountryCode` | body | `string` | no |
| `destinationCountryCode` | body | `string` | no |
| `destinationPostCode` | body | `string` | no |
| `shippingDate` | body | `date` | no |
| `courierCode[]` | body | `array<string>` | no |
| `courierName` | body | `string` | no |
| `orderNumber` | body | `string` | no |
| `title` | body | `string` | no |
| `trackingUrl` | body | `string` | no |
| `recipient.name` | body | `string` | no |
| `recipient.email` | body | `string` | no |
| `settings.restrictTrackingToCourierCode` | body | `boolean` | no |
