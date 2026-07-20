# List Partner App Orders with Cerbo

Retrieves Quest order records from Cerbo.

## Endpoint

- **Method:** `GET`
- **Path:** `/patients/:patient_id/partners/quest/orders`
- **Base URL:** `https://{tenant}.md-hq.com/api/v1`
- **Official documentation:** [List Partner App Orders](https://docs.cer.bo/#tag/Partner-Applications/operation/listPartnerAppOrders)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `patient_id` | path | `number` | no | ID of patient who orders apply to |
