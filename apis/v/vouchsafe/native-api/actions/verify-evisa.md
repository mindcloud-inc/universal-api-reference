# Verify eVisa with Vouchsafe

Verifies a UK eVisa in Vouchsafe.

## Endpoint

- **Method:** `POST`
- **Path:** `/verify/evisa`
- **Base URL:** `https://app.vouchsafe.id/api/v1`
- **Official documentation:** [Verify eVisa](https://help.vouchsafe.id/en/articles/11882037-how-do-i-use-the-evisa-verification-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `sub_type` | body | `list` | yes | The type of eVisa verification to perform. Accepted values: `ImmigrationStatus`, `RightToRent`, `RightToWork`. |
| `payload` | body | `object` | no | The verification payload. |
| `payload.reason` | body | `string` | no | Reason for the verification when using Immigration Status. |
| `payload.job_title` | body | `string` | no | Job title of the person being verified when using Immigration Status. |
| `payload.role` | body | `list` | no | Role of the person requesting the verification when using Right To Rent. Accepted values: `Agent`, `Landlord`. |
| `payload.company_name` | body | `string` | yes | Name of the company requesting the verification. |
| `payload.date_of_birth` | body | `string` | yes | Date of birth in YYYY-MM-DD or ISO 8601 format. |
| `payload.share_code` | body | `string` | yes | The 9-character share code from the UK Home Office. |
