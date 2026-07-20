# Add Patient Laboratory with Cerbo

Adds a patient laboratory record in Cerbo.

## Endpoint

- **Method:** `POST`
- **Path:** `/patients/:patient_id/laboratories`
- **Base URL:** `https://{tenant}.md-hq.com/api/v1`
- **Official documentation:** [Add Patient Laboratory](https://docs.cer.bo/#tag/Patient-FacilitiesSpecialists/operation/createPatientFacility)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `patient_id` | path | `number` | yes | ID of the patient |
| `laboratory_id` | body | `number` | yes | An integer, the laboratory ID to add. See the "Facility Endpoints" documentation for how to find the ID in the master laboratories database |
| `priority_order` | body | `number` | no | An integer representing where in the patient's laboratories list this entry should go (lowest number is considered the first/preferred listing). If null, the system will look at set_as_primary instead. |
| `set_as_primary` | body | `boolean` | no | A boolean value representing if this should be added as the patient's new preferred listing, or just added to the bottom of the list. If priority_order is set, this argument will be ignored. |
| `note` | body | `string` | no | A string, 255 character max |
