# Get Order Info with Cloudprinter.com

Retrieves order details from Cloudprinter.com.

## Endpoint

- **Method:** `POST`
- **Path:** `/cloudcore/1.0/orders/info`
- **Base URL:** `https://api.cloudprinter.com`
- **Official documentation:** [Get Order Info](https://docs.cloudprinter.com/client/cloudprinter-core-api-v1-0#get-order-info)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `reference` | body | `string` | yes | Client order reference. |
