# Create Policy with VdoCipher

Creates a new policy in VdoCipher.

## Endpoint

- **Method:** `POST`
- **Path:** `/policy`
- **Base URL:** `https://dev.vdocipher.com/api`
- **Official documentation:** [Create Policy](https://www.vdocipher.com/docs/swagger/index.html)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `domainWhitelistMode` | body | `string` | no |
| `domainWhitelistOverride` | body | `string` | no |
| `domainWhitelistValues` | body | `string` | no |
| `geoEffect` | body | `string` | no |
| `geoList` | body | `string` | no |
| `name` | body | `string` | no |
| `rentalDuration` | body | `string` | no |
| `ttl` | body | `string` | no |
| `watermarkTemplate` | body | `string` | no |
