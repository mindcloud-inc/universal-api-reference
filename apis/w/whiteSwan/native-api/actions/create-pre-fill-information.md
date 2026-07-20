# Create Pre-Fill Information with White Swan

Creates application pre-fill information in White Swan.

## Endpoint

- **Method:** `POST`
- **Path:** `/new_prefill_info`
- **Base URL:** `https://app.whiteswan.io/api/1.1/wf`
- **Official documentation:** [Create Pre-Fill Information](https://docs.whiteswan.io/partner-knowledge-base/api-documentation/action-calls/create-pre-fill-information)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `requests_ids[]` | body | `array<string>` | no | Plan request IDs to attach this pre-fill payload to. |
| `first_name` | body | `string` | no | Applicant first name. |
| `middle_name` | body | `string` | no | Applicant middle name. |
| `last_name` | body | `string` | no | Applicant last name. |
| `gender` | body | `string` | no | Applicant gender. |
| `date_of_birth` | body | `string` | no | Applicant date of birth in White Swan format. |
| `phone` | body | `string` | no | Applicant phone number. |
| `email` | body | `string` | no | Applicant email address. |
| `address` | body | `string` | no | Applicant mailing address. |
| `marital_status` | body | `string` | no | Applicant marital status. |
| `owner_estimated_income` | body | `number` | no | Estimated annual income for the owner. |
| `household_total_assets` | body | `number` | no | Total household assets. |
