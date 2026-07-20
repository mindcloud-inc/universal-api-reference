# Update Company with Twenty

## Endpoint

- **Method:** `PATCH`
- **Path:** `/rest/companies/:id`
- **Base URL:** `https://api.twenty.com`
- **Official documentation:** [Update Company](https://docs.twenty.com/developers/extend/api)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string` | yes |
| `domainName.primaryLinkLabel` | body | `string` | no |
| `domainName.primaryLinkUrl` | body | `string` | no |
| `domainName.secondaryLinks[]` | body | `array<string>` | no |
| `name` | body | `string` | no |
| `xLink.primaryLinkLabel` | body | `string` | no |
| `xLink.primaryLinkUrl` | body | `string` | no |
| `xLink.secondaryLinks[]` | body | `array<string>` | no |
| `employees` | body | `number` | no |
| `idealCustomerProfile` | body | `boolean` | no |
| `address.addressStreet1` | body | `string` | no |
| `address.addressStreet2` | body | `string` | no |
| `address.addressCity` | body | `string` | no |
| `address.addressPostcode` | body | `string` | no |
| `address.addressState` | body | `string` | no |
| `address.addressCountry` | body | `string` | no |
| `linkedinLink.primaryLinkLabel` | body | `string` | no |
| `linkedinLink.primaryLinkUrl` | body | `string` | no |
| `linkedinLink.secondaryLinks[]` | body | `array<string>` | no |
| `accountOwnerId` | body | `string` | no |
