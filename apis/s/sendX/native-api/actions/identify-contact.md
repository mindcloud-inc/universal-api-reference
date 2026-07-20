# Identify Contact with SendX

## Endpoint

- **Method:** `POST`
- **Path:** `/contact/identify`
- **Base URL:** `https://api.sendx.io/api/v1/rest`
- **Official documentation:** [Identify Contact](https://docs.sendx.io/api-reference/getting-started/identify-contact)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `email` | body | `string` | yes |
| `firstName` | body | `string` | no |
| `lastName` | body | `string` | no |
| `company` | body | `string` | no |
| `customFields` | body | `object` | no |
| `tags[]` | body | `array<string>` | no |
| `lists[]` | body | `array<string>` | no |
| `newEmail` | body | `string` | no |
