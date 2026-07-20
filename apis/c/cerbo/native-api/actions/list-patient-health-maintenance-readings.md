# List Patient Health Maintenance Readings with Cerbo

Retrieves patient health maintenance readings from Cerbo.

## Endpoint

- **Method:** `GET`
- **Path:** `/patients/:patient_id/health_maintenance`
- **Base URL:** `https://{tenant}.md-hq.com/api/v1`
- **Official documentation:** [List Patient Health Maintenance Readings](https://docs.cer.bo/#tag/Patient-Health-Maintenance/operation/showPatientHealthMaintenance)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `patient_id` | path | `number` | no | ID of patient |
