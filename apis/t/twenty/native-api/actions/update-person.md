# Update Person with Twenty

## Endpoint

- **Method:** `PATCH`
- **Path:** `/rest/people/:id`
- **Base URL:** `https://api.twenty.com`
- **Official documentation:** [Update Person](https://docs.twenty.com/developers/extend/api)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string` | yes |
| `phones.primaryPhoneNumber` | body | `string` | no |
| `phones.primaryPhoneCountryCode` | body | `string` | no |
| `phones.primaryPhoneCallingCode` | body | `string` | no |
| `phones.additionalPhones[]` | body | `array<string>` | no |
| `name.firstName` | body | `string` | no |
| `name.lastName` | body | `string` | no |
| `emails.primaryEmail` | body | `string` | no |
| `emails.additionalEmails[]` | body | `array<string>` | no |
| `city` | body | `string` | no |
| `xLink.primaryLinkLabel` | body | `string` | no |
| `xLink.primaryLinkUrl` | body | `string` | no |
| `xLink.secondaryLinks[]` | body | `array<string>` | no |
| `jobTitle` | body | `string` | no |
| `linkedinLink.primaryLinkLabel` | body | `string` | no |
| `linkedinLink.primaryLinkUrl` | body | `string` | no |
| `linkedinLink.secondaryLinks[]` | body | `array<string>` | no |
| `companyId` | body | `string` | no |
