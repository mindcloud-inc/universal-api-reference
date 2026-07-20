# Track COD Shipment with iPaymu

Track the status of an iPaymu cash-on-delivery shipment.

## Endpoint

- **Method:** `POST`
- **Path:** `/cod/tracking`
- **Base URL:** `https://my.ipaymu.com/api/v2`
- **Official documentation:** [Track COD Shipment](https://ipaymu.com/api-collection/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `awb` | body | `string` | yes | Air waybill / tracking number. |
| `transaction_id` | body | `string` | yes | COD transaction identifier. |
