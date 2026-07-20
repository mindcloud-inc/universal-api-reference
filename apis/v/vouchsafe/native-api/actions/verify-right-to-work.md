# Verify Right To Work with Vouchsafe

Verifies right to work with a UK eVisa in Vouchsafe.

## Endpoint

- **Method:** `POST`
- **Path:** `/verify/evisa`
- **Base URL:** `https://app.vouchsafe.id/api/v1`
- **Official documentation:** [Verify Right To Work](https://help.vouchsafe.id/en/articles/11882037-how-do-i-use-the-evisa-verification-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `payload` | body | `object` | no | The right to work verification payload. |
| `payload.company_name` | body | `string` | yes | Name of the company requesting the verification. |
| `payload.date_of_birth` | body | `string` | yes | Date of birth in YYYY-MM-DD or ISO 8601 format. |
| `payload.share_code` | body | `string` | yes | The 9-character share code from the UK Home Office. |
