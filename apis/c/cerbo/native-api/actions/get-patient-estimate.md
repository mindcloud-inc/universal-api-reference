# Get Patient Estimate with Cerbo

Retrieves patient estimate details from Cerbo.

## Endpoint

- **Method:** `GET`
- **Path:** `/patients/:pt_id/estimates/:estimate_id`
- **Base URL:** `https://{tenant}.md-hq.com/api/v1`
- **Official documentation:** [Get Patient Estimate](https://docs.cer.bo/#tag/Patient-Charges/operation/showPatientEstimate)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `pt_id` | path | `number` | no |
| `estimate_id` | path | `number` | no |
