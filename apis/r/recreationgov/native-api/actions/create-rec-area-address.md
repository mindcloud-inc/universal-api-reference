# Create Rec Area Address with Recreation.gov

Creates a recreation area address in Recreation.gov.

## Endpoint

- **Method:** `POST`
- **Path:** `/recareas/{id}/recareaaddresses`
- **Base URL:** `https://ridb.recreation.gov/api/v1`
- **Official documentation:** [Create Rec Area Address](https://ridb.recreation.gov/shared/swagger/dataSteward.yaml)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `number` | yes |
| `type` | body | `string` | no |
| `address1` | body | `string` | no |
| `address2` | body | `string` | no |
| `address3` | body | `string` | no |
| `city` | body | `string` | no |
| `postalCode` | body | `string` | no |
| `stateCode` | body | `string` | yes |
| `countryCode` | body | `string` | yes |
