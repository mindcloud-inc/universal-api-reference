# List Patient Pharmacies with Cerbo

Retrieves patient pharmacies from Cerbo.

## Endpoint

- **Method:** `GET`
- **Path:** `/patients/:patient_id/pharmacies`
- **Base URL:** `https://{tenant}.md-hq.com/api/v1`
- **Official documentation:** [List Patient Pharmacies](https://docs.cer.bo/#tag/Patient-FacilitiesSpecialists/operation/listPatientPharmacies)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `patient_id` | path | `number` | yes | The patient ID |
