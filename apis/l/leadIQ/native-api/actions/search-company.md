# Search Company with LeadIQ

## Endpoint

- **Method:** `POST`
- **Path:** `graphql`
- **Base URL:** `https://api.leadiq.com/`
- **Official documentation:** [Search Company](https://developer.leadiq.com/#query-searchCompany)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `variables.input.id` | body | `string` | no | Search by the LeadIQ company identifier. |
| `variables.input.name` | body | `string` | no | Search by company name. |
| `variables.input.domain` | body | `string` | no | Search by company domain, for example leadiq.com. |
| `variables.input.linkedinId` | body | `string` | no | Search by the LinkedIn company ID. |
| `variables.input.linkedinUrl` | body | `string` | no | Search by the LinkedIn company URL. |
| `variables.input.strict` | body | `boolean` | no | When true, require a stricter match against the identifiers you provide. |
