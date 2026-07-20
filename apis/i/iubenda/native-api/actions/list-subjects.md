# List Subjects with iubenda

Retrieves subjects from iubenda.

## Endpoint

- **Method:** `GET`
- **Path:** `/subjects`
- **Base URL:** `https://consent.iubenda.com`
- **Official documentation:** [List Subjects](https://www.iubenda.com/en/help/6484-consent-solution-http-api-documentation/#subjects)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | query | `string` | no | Filter by an exact subject ID. |
| `email_exact` | query | `string` | no | Filter by an exact subject email address. |
| `first_name` | query | `string` | no | Filter by an exact subject first name. |
| `last_name` | query | `string` | no | Filter by an exact subject last name. |
| `verified` | query | `boolean` | no | Filter by verified status. |
| `phone` | query | `string` | no | Filter subjects containing the given phone number with country code. |
| `from_time` | query | `string` | no | Return subjects from this timestamp onward. |
| `to_time` | query | `string` | no | Return subjects up to this timestamp. |
| `starting_after` | query | `string` | no | Cursor indicating after which subject results should be returned. |
| `limit` | query | `number` | no | Maximum number of subjects to return. |
