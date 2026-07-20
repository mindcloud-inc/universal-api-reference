# Get Charge Refund with OPN

Retrieves details for a charge refund from OPN.

## Endpoint

- **Method:** `GET`
- **Path:** `/charges/:id/refunds/:refundId`
- **Base URL:** `https://api.omise.co`
- **Official documentation:** [Get Charge Refund](https://docs.omise.co/refunds-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The charge ID that owns the refund. |
| `refundId` | path | `string` | yes | The refund ID to retrieve. |
