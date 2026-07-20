# Confirm Redemption By Transaction ID with Vouchery.io

## Endpoint

- **Method:** `PUT`
- **Path:** `/redemptions/confirm`
- **Base URL:** `https://mindcloud.sandbox.vouchery.app/api/v2.1`
- **Official documentation:** [Confirm Redemption By Transaction ID](https://docs.vouchery.io/reference/putapiv21redemptionsconfirm)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `confirmed` | body | `boolean` | no | Whether the redemption is confirmed |
| `transaction_id` | query | `string` | yes | Transaction ID |
