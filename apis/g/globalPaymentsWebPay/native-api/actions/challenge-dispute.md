# Challenge Dispute with Global Payments WebPay

Updates a dispute by challenging it in Global Payments WebPay.

## Endpoint

- **Method:** `POST`
- **Path:** `/disputes/{id}/challenge`
- **Base URL:** `https://apis.globalpay.com/ucp`
- **Official documentation:** [Challenge Dispute](https://developer.globalpayments.com/api/disputes)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Global Payments dispute ID. |
