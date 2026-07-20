# Get Order Status with Split CSV

Retrieves the status of an order in Split CSV.

## Endpoint

- **Method:** `GET`
- **Path:** `/app/api/v1/orders/:id/status`
- **Base URL:** `https://www.splitcsv.com`
- **Official documentation:** [Get Order Status](https://www.splitcsv.com/developers/core/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The order ID returned by Create Order. Use latest to retrieve the most recent order. |
