# Get Patient Order with Cerbo

Retrieves patient order details from Cerbo.

## Endpoint

- **Method:** `GET`
- **Path:** `/patients/:patient_id/orders/:order_id`
- **Base URL:** `https://{tenant}.md-hq.com/api/v1`
- **Official documentation:** [Get Patient Order](https://docs.cer.bo/#tag/Patient-Orders/operation/showPatientOrder)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `patient_id` | path | `number` | no | ID of patient |
| `order_id` | path | `number` | no | ID of patient |
