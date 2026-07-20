# Create Survey Package Instance with Castor EDC

Creates a survey package instance in Castor EDC.

## Endpoint

- **Method:** `POST`
- **Path:** `/study/:study_id/survey-package-instance`
- **Base URL:** `https://us.castoredc.com/api`
- **Official documentation:** [Create Survey Package Instance](https://us.castoredc.com/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `study_id` | path | `string` | yes | The Castor study UUID. |
| `survey_package_id` | body | `string` | yes | The survey package UUID to instantiate. |
| `participant_id` | body | `string` | no | Participant UUID to receive the survey package instance. |
| `ccr_patient_id` | body | `string` | no | CCR patient identifier to receive the survey package instance. |
| `email_address` | body | `string` | no | Optional email address to send the invitation to. |
| `package_invitation_subject` | body | `string` | no | Optional subject for the invitation email. |
| `package_invitation` | body | `string` | no | Optional invitation email body; include {url} if you want Castor to send it from this request. |
| `available_from` | body | `string` | no | UTC datetime when the survey package instance becomes available or is scheduled to send. |
| `auto_lock_on_finish` | body | `boolean` | no | Lock the survey package instance automatically when the respondent finishes. |
| `parent_type` | body | `string` | no | Parent type: 0 none, 1 visit, 2 repeating data instance. |
| `parent_id` | body | `string` | no | Optional UUID of the parent visit or repeating data instance. |
