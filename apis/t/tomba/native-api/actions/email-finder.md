# Email Finder with Tomba

Finds a contact email in Tomba.

## Endpoint

- **Method:** `GET`
- **Path:** `/email-finder`
- **Base URL:** `https://api.tomba.io/v1`
- **Official documentation:** [Email Finder](https://docs.tomba.io/api/finder#email-finder)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `domain` | query | `string` | yes | Domain to search for the contact. |
| `company` | query | `string` | no | Company name to search when a domain is not available. |
| `full_name` | query | `string` | yes | Full name of the contact to look up. |
| `first_name` | query | `string` | no | First name of the contact. |
| `last_name` | query | `string` | no | Last name of the contact. |
| `enrich_mobile` | query | `boolean` | no | Include phone data when available. |
