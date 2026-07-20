# Create Secure Message with Cerbo

Creates a secure patient message in Cerbo.

## Endpoint

- **Method:** `POST`
- **Path:** `/patients/:patient_id/portal/secure_messages`
- **Base URL:** `https://{tenant}.md-hq.com/api/v1`
- **Official documentation:** [Create Secure Message](https://docs.cer.bo/#tag/Secure-Messages/operation/createSecureMessage)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `patient_id` | path | `number` | no | — |
| `subject` | body | `string` | yes | between 1 and 54 characters long |
| `note` | body | `string` | yes | at least 10 characters long |
| `dr_id` | body | `number` | no | A valid ID of a non-archived, non-resource user who should respond to the message |
| `reply` | body | `string` | no | how the patient would like to receive a response |
