# List Secure Messages with Cerbo

Retrieves secure patient messages from Cerbo.

## Endpoint

- **Method:** `GET`
- **Path:** `/patients/:patient_id/portal/secure_messages`
- **Base URL:** `https://{tenant}.md-hq.com/api/v1`
- **Official documentation:** [List Secure Messages](https://docs.cer.bo/#tag/Secure-Messages/operation/listSecureMessages)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `patient_id` | path | `number` | no | — |
| `sent_by` | query | `string` | no | Either “pt” (to get all messages sent by the patient) or “dr” (to get all messages sent to the patient from doctor/clinic) |
