# Search People with LeadIQ

## Endpoint

- **Method:** `POST`
- **Path:** `graphql`
- **Base URL:** `https://api.leadiq.com/`
- **Official documentation:** [Search People](https://developer.leadiq.com/#query-searchPeople)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `variables.input.id` | body | `string` | no | Search by the LeadIQ person identifier. |
| `variables.input.firstName` | body | `string` | no | Search by first name. |
| `variables.input.lastName` | body | `string` | no | Search by last name. |
| `variables.input.fullName` | body | `string` | no | Search by a person's full name. |
| `variables.input.email` | body | `string` | no | Search by email address. |
| `variables.input.phone` | body | `string` | no | Search by phone number. |
| `variables.input.linkedinId` | body | `string` | no | Search by the LinkedIn member ID. |
| `variables.input.linkedinUrl` | body | `string` | no | Search by the LinkedIn profile URL. |
| `variables.input.company` | body | `object` | no | Optional CompanyDetails object. Supported keys: companyId, name, domain, emailDomain, linkedinId, country, searchInPastCompanies, strict. |
| `variables.input.middleName` | body | `string` | no | Search by middle name. |
| `variables.input.hashedEmail` | body | `string` | no | Search by a SHA256 hashed email address. |
| `variables.input.workEmailStatusIn[]` | body | `array<string>` | no | Optional array of email verification statuses: Verified, Unverified, VerifiedLikely, Invalid. |
| `variables.input.containsWorkContactInfo` | body | `boolean` | no | When true, only return people with work contact info. |
| `variables.input.profileFilter[]` | body | `array<string>` | no | Optional array of profile filters: HasVerifiedWorkPhone, HasPersonalPhone, HasWorkPhone, HasPersonalEmail, HasVerifiedWorkEmail, HasWorkEmail. |
| `variables.input.includeInvalid` | body | `boolean` | no | When true, include Invalid emails in the result. |
| `variables.input.qualityFilter` | body | `object` | no | Optional QualityFilter object. Currently supports the phone enum quality filter. |
| `variables.input.minConfidence` | body | `number` | no | Minimum person confidence score from 0 to 100. |
| `variables.input.limit` | body | `number` | no | Maximum number of people to return. |
| `variables.input.skip` | body | `number` | no | Number of matching people to skip before returning results. |
