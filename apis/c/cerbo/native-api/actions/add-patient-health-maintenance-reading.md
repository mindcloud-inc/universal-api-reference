# Add Patient Health Maintenance Reading with Cerbo

Adds a patient health maintenance reading in Cerbo.

## Endpoint

- **Method:** `POST`
- **Path:** `/patients/:patient_id/health_maintenance/:health_maintenance_id`
- **Base URL:** `https://{tenant}.md-hq.com/api/v1`
- **Official documentation:** [Add Patient Health Maintenance Reading](https://docs.cer.bo/#tag/Patient-Health-Maintenance/operation/createPatientHealthMaintenance)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `patient_id` | path | `number` | yes | ID of patient |
| `health_maintenance_id` | path | `number` | yes | ID of health maintenance entry *See “HEALTH MAINTENANCE ENDPOINTS” documentation to get definitions from the master health maintenance trackers list |
| `date` | body | `string` | yes | A string specifying the date of the health maintenance tracker. |
| `notes` | body | `number` | no | A string |
