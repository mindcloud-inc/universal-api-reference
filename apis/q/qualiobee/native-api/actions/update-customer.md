# Update Customer with Qualiobee

Updates an existing customer in Qualiobee.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/:organizationUuid/customer/:customerUuid`
- **Base URL:** `https://app.qualiobee.fr/api`
- **Official documentation:** [Update Customer](https://app.qualiobee.fr/api/doc/#/Customer/PublicCustomerController_updateOne)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `organizationUuid` | path | `string` | yes |
| `customerUuid` | path | `string` | yes |
| `name` | body | `string` | no |
| `firstName` | body | `string` | no |
| `lastName` | body | `string` | no |
| `email` | body | `string` | no |
| `phoneNumber` | body | `string` | no |
| `siret` | body | `string` | no |
| `naf` | body | `string` | no |
| `note` | body | `string` | no |
| `location.addressLine1` | body | `string` | no |
| `location.addressLine2` | body | `string` | no |
| `location.postCode` | body | `string` | no |
| `location.city` | body | `string` | no |
| `location.country` | body | `string` | no |
