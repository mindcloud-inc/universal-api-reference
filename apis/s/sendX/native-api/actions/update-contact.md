# Update Contact with SendX

## Endpoint

- **Method:** `PUT`
- **Path:** `/contact/:identifier`
- **Base URL:** `https://api.sendx.io/api/v1/rest`
- **Official documentation:** [Update Contact](https://docs.sendx.io/api-reference/contact/update-contact)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `identifier` | path | `string` | yes |
| `email` | body | `string` | yes |
| `firstName` | body | `string` | no |
| `lastName` | body | `string` | no |
| `company` | body | `string` | no |
| `customFields` | body | `object` | no |
| `lists[]` | body | `array<string>` | no |
| `tags[]` | body | `array<string>` | no |
| `lastTrackedIp` | body | `string` | no |
