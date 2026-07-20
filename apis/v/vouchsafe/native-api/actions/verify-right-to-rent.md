# Verify Right To Rent with Vouchsafe

Verifies right to rent with a UK eVisa in Vouchsafe.

## Endpoint

- **Method:** `POST`
- **Path:** `/verify/evisa`
- **Base URL:** `https://app.vouchsafe.id/api/v1`
- **Official documentation:** [Verify Right To Rent](https://help.vouchsafe.id/en/articles/11882037-how-do-i-use-the-evisa-verification-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `payload` | body | `object` | no | The right to rent verification payload. |
| `payload.role` | body | `list` | yes | Role of the person requesting the verification. Accepted values: `Agent`, `Landlord`. |
| `payload.company_name` | body | `string` | yes | Name of the company or agency requesting the verification. |
| `payload.date_of_birth` | body | `string` | yes | Date of birth in YYYY-MM-DD or ISO 8601 format. |
| `payload.share_code` | body | `string` | yes | The 9-character share code from the UK Home Office. |
