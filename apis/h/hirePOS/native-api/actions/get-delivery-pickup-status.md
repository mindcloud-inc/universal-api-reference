# Get Delivery Pickup Status with HirePOS

Retrieves delivery and pickup status for an invoice from HirePOS.

## Endpoint

- **Method:** `GET`
- **Path:** `/DeliveryPickupStatus`
- **Base URL:** `https://api.hirepos.com`
- **Official documentation:** [Get Delivery Pickup Status](https://docs.hirepos.com/en/articles/9534913)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `InvoiceNo` | query | `string` | yes | Invoice number to retrieve delivery and pickup status for. |
