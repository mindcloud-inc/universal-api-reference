# List Patient Subscriptions with Cerbo

Retrieves patient subscriptions from Cerbo.

## Endpoint

- **Method:** `GET`
- **Path:** `/patients/:patient_id/subscriptions`
- **Base URL:** `https://{tenant}.md-hq.com/api/v1`
- **Official documentation:** [List Patient Subscriptions](https://docs.cer.bo/#tag/Patient-Subscriptions/operation/showPatientSubscriptions)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `patient_id` | path | `number` | no | ID of patient |
| `include_deleted` | query | `boolean` | no | False by default. Returns deleted and current subscriptions if set to true. |
