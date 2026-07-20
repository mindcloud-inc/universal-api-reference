# Request Verification with Vouchsafe

Creates a verification request in Vouchsafe.

## Endpoint

- **Method:** `POST`
- **Path:** `/verifications`
- **Base URL:** `https://app.vouchsafe.id/api/v1`
- **Official documentation:** [Request Verification](https://help.vouchsafe.id/en/articles/11979589-quick-start-guide)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | yes | The user's email address. |
| `expires_at` | body | `string` | no | When the verification session expires as an ISO 8601 timestamp. |
| `external_id` | body | `string` | no | An identifier from your own systems. |
| `first_name` | body | `string` | no | The user's first name, if you have it. |
| `last_name` | body | `string` | no | The user's last name, if you have it. |
| `postcode` | body | `string` | no | The user's postcode, if you have it. |
| `redirect_url` | body | `string` | no | A URL to send the user back to upon success. |
| `street_address` | body | `string` | no | The user's street address, if you have it. |
| `workflow_id` | body | `string` | no | Which verification flow to use. |
| `date_of_birth` | body | `string` | no | The user's date of birth in YYYY-MM-DD or ISO 8601 format. |
