# Verify Immigration Status with Vouchsafe

Verifies immigration status with a UK eVisa in Vouchsafe.

## Endpoint

- **Method:** `POST`
- **Path:** `/verify/evisa`
- **Base URL:** `https://app.vouchsafe.id/api/v1`
- **Official documentation:** [Verify Immigration Status](https://help.vouchsafe.id/en/articles/11882037-how-do-i-use-the-evisa-verification-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `payload` | body | `object` | no | The immigration status verification payload. |
| `payload.reason` | body | `string` | yes | Reason for the verification. |
| `payload.job_title` | body | `string` | yes | Job title of the person being verified. |
| `payload.company_name` | body | `string` | yes | Name of the company requesting the verification. |
| `payload.date_of_birth` | body | `string` | yes | Date of birth in YYYY-MM-DD or ISO 8601 format. |
| `payload.share_code` | body | `string` | yes | The 9-character share code from the UK Home Office. |
