# Save Contact with Charla

Saves a contact record in Charla.

## Endpoint

- **Method:** `POST`
- **Path:** `/contacts`
- **Base URL:** `https://api.charla.com/v1`
- **Official documentation:** [Save Contact](https://charla.com/public-api.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `browser_language` | body | `string` | no | Browser language used by the visitor. |
| `country_code` | body | `string` | no | Country code in ISO 3166-1 format. |
| `email` | body | `string` | no | Email of the visitor if available. |
| `id` | body | `string` | no | Provide an existing contact ID to update that contact. |
| `ip` | body | `string` | no | IP address of the visitor. |
| `location` | body | `string` | no | Location of the visitor. |
| `name` | body | `string` | no | Name of the visitor if available. |
| `phone` | body | `string` | no | Phone of the visitor if available. |
| `platform` | body | `string` | no | Device or platform used by the visitor. |
