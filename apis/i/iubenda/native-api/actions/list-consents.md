# List Consents with iubenda

Retrieves consents from iubenda.

## Endpoint

- **Method:** `GET`
- **Path:** `/consent`
- **Base URL:** `https://consent.iubenda.com`
- **Official documentation:** [List Consents](https://www.iubenda.com/en/help/6484-consent-solution-http-api-documentation/#consent)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `subject_id` | query | `string` | no | Filter by subject ID. |
| `subject_email_exact` | query | `string` | no | Filter by an exact subject email address. |
| `subject_first_name` | query | `string` | no | Filter by an exact subject first name. |
| `subject_last_name` | query | `string` | no | Filter by an exact subject last name. |
| `subject_verified` | query | `boolean` | no | Filter by subject verified status. |
| `source` | query | `string` | no | Filter by consent source: public or private. |
| `ip_address` | query | `string` | no | Filter by IP address. |
| `from_time` | query | `string` | no | Return consents from this timestamp onward. |
| `to_time` | query | `string` | no | Return consents up to this timestamp. |
| `starting_after` | query | `string` | no | Cursor indicating after which consent results should be returned. |
| `limit` | query | `number` | no | Maximum number of consents to return. |
