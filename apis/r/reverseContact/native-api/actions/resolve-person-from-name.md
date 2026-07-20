# Resolve Person From Name with Reverse Contact

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/resolve/persons/name`
- **Base URL:** `https://api.reversecontact.com`
- **Official documentation:** [Resolve Person From Name](https://app.reversecontact.com/docs/endpoints/resolve-person-name)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `firstName` | body | `string` | yes | Person first name. |
| `lastName` | body | `string` | yes | Person last name. |
| `companyDomain` | body | `string` | no | Company domain. Provide this or company name. |
| `companyName` | body | `string` | no | Company name. Provide this or company domain. |
| `webhookUrl` | body | `string` | no | HTTPS callback URL for async results. |
