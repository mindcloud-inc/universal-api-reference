# List Patient Orders with Cerbo

Retrieves patient orders from Cerbo.

## Endpoint

- **Method:** `GET`
- **Path:** `/patients/:patient_id/orders`
- **Base URL:** `https://{tenant}.md-hq.com/api/v1`
- **Official documentation:** [List Patient Orders](https://docs.cer.bo/#tag/Patient-Orders/operation/listPatientOrders)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `patient_id` | path | `number` | no | ID of patient |
