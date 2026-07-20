# Update Patient with Cerbo

Updates an existing patient in Cerbo.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/patients/:patient_id`
- **Base URL:** `https://{tenant}.md-hq.com/api/v1`
- **Official documentation:** [Update Patient](https://docs.cer.bo/#tag/Patients/operation/updatePatient)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `patient_id` | path | `number` | yes | ID of the patient to update |
| `first_name` | body | `string` | no | — |
| `last_name` | body | `string` | no | — |
| `dob` | body | `string` | no | YYYY-MM-DD |
| `sex` | body | `string` | no | must be 'M', 'F', or '?' |
| `inactive` | body | `string` | no | Sets the patient status. Accepts the following values: \| Value \| Result \| \|---\|---\| \| `"prospective"` or `"-1"` \| Prospective patient \| \| `"0"`, empty, or omitted \| Active patient (default) \| \| `"inactive"` or `"1"` \| Inactive patient \| \| `"deceased"` or `"dead"` or `"2"` \| Deceased patient \| **Important — GET response behavior:** When reading patient data via GET, the `inactive` field is cast to a boolean rather than returning the original value. This means: \| Stored status \| `inactive` in GET \| `patient_status_description` in GET \| \|---\|---\|---\| \| Prospective (`-1`) \| `true` \| `"prospective"` \| \| Active (`0`) \| `false` \| `"active"` \| \| Inactive (`1`) \| `true` \| `"inactive"` \| \| Deceased (`2`) \| `true` \| `"deceased"` \| Because `inactive` returns `true` for prospective, inactive, and deceased patients alike, you **must** use the `patient_status_description` field to determine the actual status. This is a known legacy serialization issue where the create/update and read representations differ. |
