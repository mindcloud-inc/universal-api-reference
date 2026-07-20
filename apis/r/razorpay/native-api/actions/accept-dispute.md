# Accept Dispute with Razorpay

Accepts a dispute in Razorpay as lost.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/disputes/:id/accept`
- **Base URL:** `https://api.razorpay.com`
- **Official documentation:** [Accept Dispute](https://razorpay.com/docs/api/disputes/accept/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Unique identifier of the dispute. |
