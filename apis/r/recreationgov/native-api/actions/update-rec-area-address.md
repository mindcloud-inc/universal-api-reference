# Update Rec Area Address with Recreation.gov

Updates a recreation area address in Recreation.gov.

## Endpoint

- **Method:** `PUT`
- **Path:** `/recareas/{id}/recareaaddresses/{addressId}`
- **Base URL:** `https://ridb.recreation.gov/api/v1`
- **Official documentation:** [Update Rec Area Address](https://ridb.recreation.gov/shared/swagger/dataSteward.yaml)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `number` | yes |
| `type` | body | `string` | no |
| `address1` | body | `string` | no |
| `addressId` | path | `number` | yes |
| `address2` | body | `string` | no |
| `address3` | body | `string` | no |
| `city` | body | `string` | no |
| `postalCode` | body | `string` | no |
| `stateCode` | body | `string` | yes |
| `countryCode` | body | `string` | yes |
