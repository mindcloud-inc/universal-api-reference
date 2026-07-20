# Send Location with Ziper

Sends a WhatsApp location message with Ziper.

## Endpoint

- **Method:** `POST`
- **Path:** `/send.php`
- **Base URL:** `https://ziper.io/api`
- **Official documentation:** [Send Location](https://documenter.getpostman.com/view/2881191/VUqmvyob)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `number` | query | `string` | yes | WhatsApp phone number in country-code plus phone-number format. |
| `location.degreesLatitude` | body | `number` | yes | Location latitude in decimal degrees. |
| `location.degreesLongitude` | body | `number` | yes | Location longitude in decimal degrees. |
