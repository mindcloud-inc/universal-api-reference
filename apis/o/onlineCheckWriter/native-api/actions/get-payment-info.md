# Get Payment Info with OnlineCheckWriter

Retrieves the status and details of a specific payment.

## Endpoint

- **Method:** `GET`
- **Path:** `/send-payment/:paymentId/info`
- **Base URL:** `https://test.onlinecheckwriter.com/api/v3`
- **Official documentation:** [Get Payment Info](https://apiv3.onlinecheckwriter.com)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `paymentId` | path | `string` | yes | The payment identifier. |
