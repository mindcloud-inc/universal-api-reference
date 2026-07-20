# Stop Rebilling with Digistore24

Stops rebilling for a Digistore24 purchase.

## Endpoint

- **Method:** `POST`
- **Path:** `/stopRebilling`
- **Base URL:** `https://www.digistore24.com/api/call`
- **Official documentation:** [Stop Rebilling](https://digistore24.com/api/docs/paths/stopRebilling.yaml)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `purchase_id` | query | `string` | yes | Purchase ID |
| `force` | query | `boolean` | no | Force stop |
| `ignore_refund_possibility` | query | `boolean` | no | Ignore refund possibility |
