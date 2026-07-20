# Request Rates with Easyship

Retrieves shipping rates from Easyship.

## Endpoint

- **Method:** `POST`
- **Path:** `/rates`
- **Base URL:** `https://public-api.easyship.com/2024-09`
- **Official documentation:** [Request Rates](https://developers.easyship.com/reference/rates_request)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `origin_address` | body | `object` | yes | Origin address object for the shipment rate request. |
| `destination_address` | body | `object` | yes | Destination address object for the shipment rate request. |
| `parcels[]` | body | `array<object>` | yes | Parcels array for the shipment rate request. |
