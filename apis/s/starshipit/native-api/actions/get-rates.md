# Get Rates with Starshipit

## Endpoint

- **Method:** `POST`
- **Path:** `/rates`
- **Base URL:** `https://api.starshipit.com/api`
- **Official documentation:** [Get Rates](https://api-docs.starshipit.com/#03ce0c71-af60-4e3a-a967-451515dea9f6)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `sender.street` | body | `string` | no |
| `sender.suburb` | body | `string` | no |
| `sender.city` | body | `string` | no |
| `sender.state` | body | `string` | no |
| `sender.post_code` | body | `string` | no |
| `sender.country_code` | body | `string` | no |
| `destination.street` | body | `string` | no |
| `destination.suburb` | body | `string` | no |
| `destination.city` | body | `string` | no |
| `destination.state` | body | `string` | no |
| `destination.post_code` | body | `string` | no |
| `destination.country_code` | body | `string` | no |
| `packages[]` | body | `array<object>` | no |
