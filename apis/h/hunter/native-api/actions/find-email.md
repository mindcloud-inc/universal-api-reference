# Find Email with Hunter

## Endpoint

- **Method:** `GET`
- **Path:** `/email-finder`
- **Base URL:** `https://api.hunter.io/v2`
- **Official documentation:** [Find Email](https://hunter.io/api-documentation/v2#email-finder)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `domain` | query | `string` | yes | Company domain, like hunter.io. |
| `first_name` | query | `string` | yes | Person's first name. |
| `last_name` | query | `string` | yes | Person's last name. |
| `company` | query | `string` | no | Company name when a domain is not provided. |
| `linkedin_handle` | query | `string` | no | — |
| `full_name` | query | `string` | no | — |
| `max_duration` | query | `number` | no | — |
