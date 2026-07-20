# Schedule Credential Issuance with Certifier

Schedules future credential issuance in Certifier.

## Endpoint

- **Method:** `POST`
- **Path:** `/credentials/:id/schedule`
- **Base URL:** `https://api.certifier.io/v1`
- **Official documentation:** [Schedule Credential Issuance](https://developers.certifier.io/docs/api-reference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | — |
| `issueAt` | body | `date` | no | Use an ISO 8601 date-time string. |
| `sendAtIssuance` | body | `boolean` | yes | Live runtime currently requires this flag when scheduling issuance. |
