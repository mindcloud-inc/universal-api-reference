# Send Patient Email with Cerbo

Sends an email to a Cerbo patient.

## Endpoint

- **Method:** `POST`
- **Path:** `/patients/:patient_id/emails/send`
- **Base URL:** `https://{tenant}.md-hq.com/api/v1`
- **Official documentation:** [Send Patient Email](https://docs.cer.bo/#tag/Patient-Emails/operation/sendPatientEmail)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `patient_id` | path | `number` | yes | ID of the patient to send email to |
| `subject` | body | `string` | yes | Subject of email to be sent |
| `body` | body | `string` | yes | Body of email to be sent |
| `reply-to` | body | `string` | yes | This is the address that any patient response will be forwarded to (the email itself will be sent from do-not-reply@md-hq.com). |
