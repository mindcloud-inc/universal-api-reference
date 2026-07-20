# Create Location with Jaicob

## Endpoint

- **Method:** `POST`
- **Path:** `/locations`
- **Base URL:** `https://api.jaicob.ai`
- **Official documentation:** [Create Location](https://developers.jaicob.ai/reference/create_location)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `addressLine1` | body | `string` | yes |
| `addressLine2` | body | `string` | no |
| `email` | body | `string` | no |
| `phone` | body | `string` | no |
| `postcode` | body | `string` | yes |
| `city` | body | `string` | yes |
| `country` | body | `string` | yes |
| `state` | body | `string` | yes |
| `isHeadQuarter` | body | `boolean` | yes |
| `name` | body | `string` | yes |
| `clientId` | body | `string` | no |
| `vacancyIds[]` | body | `array<string>` | no |
| `userIds[]` | body | `array<string>` | no |
