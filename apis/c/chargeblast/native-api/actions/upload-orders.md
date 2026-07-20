# Upload Orders with Chargeblast

Uploads orders to Chargeblast.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2/orders/upload`
- **Base URL:** `https://api.chargeblast.com`
- **Official documentation:** [Upload Orders](https://docs.chargeblast.com/api-reference/sync-data/upload-orders)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `orders[]` | body | `array<object>` | yes | The list of orders to upload to Chargeblast. Each order object should follow the documented OrderUploadBodyOrder contract; live runtime in this tenant also required `status` and `last4`. |
