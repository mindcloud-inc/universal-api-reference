# Create Location with Qualiobee

Creates a new location in Qualiobee.

## Endpoint

- **Method:** `POST`
- **Path:** `/:organizationUuid/location`
- **Base URL:** `https://app.qualiobee.fr/api`
- **Official documentation:** [Create Location](https://app.qualiobee.fr/api/doc/#/Location/PublicLocationController_createOne)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `organizationUuid` | path | `string` | yes |
| `addressLine1` | body | `string` | no |
| `addressLine2` | body | `string` | no |
| `postCode` | body | `string` | no |
| `city` | body | `string` | no |
| `country` | body | `string` | no |
