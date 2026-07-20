# Update Location with Qualiobee

Updates an existing location in Qualiobee.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/:organizationUuid/location/:locationUuid`
- **Base URL:** `https://app.qualiobee.fr/api`
- **Official documentation:** [Update Location](https://app.qualiobee.fr/api/doc/#/Location/PublicLocationController_updateOne)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `organizationUuid` | path | `string` | yes |
| `locationUuid` | path | `string` | yes |
| `addressLine1` | body | `string` | no |
| `addressLine2` | body | `string` | no |
| `postCode` | body | `string` | no |
| `city` | body | `string` | no |
| `country` | body | `string` | no |
