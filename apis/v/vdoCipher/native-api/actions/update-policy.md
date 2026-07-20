# Update Policy with VdoCipher

Updates an existing policy in VdoCipher.

## Endpoint

- **Method:** `PUT`
- **Path:** `/policy/:id`
- **Base URL:** `https://dev.vdocipher.com/api`
- **Official documentation:** [Update Policy](https://www.vdocipher.com/docs/swagger/index.html)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `domainWhitelistMode` | body | `string` | no |
| `domainWhitelistOverride` | body | `string` | no |
| `domainWhitelistValues` | body | `string` | no |
| `geoEffect` | body | `string` | no |
| `geoList` | body | `string` | no |
| `id` | path | `string` | no |
| `name` | body | `string` | no |
| `rentalDuration` | body | `string` | no |
| `ttl` | body | `string` | no |
| `watermarkTemplate` | body | `string` | no |
