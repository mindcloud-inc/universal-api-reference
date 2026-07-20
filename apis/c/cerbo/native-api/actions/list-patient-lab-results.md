# List Patient Lab Results with Cerbo

Retrieves patient lab results from Cerbo.

## Endpoint

- **Method:** `GET`
- **Path:** `/patients/:pt_id/lab_results`
- **Base URL:** `https://{tenant}.md-hq.com/api/v1`
- **Official documentation:** [List Patient Lab Results](https://docs.cer.bo/#tag/Patient-Lab-Results/operation/getPatientLabResults)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `pt_id` | path | `number` | no | ID of patient |
