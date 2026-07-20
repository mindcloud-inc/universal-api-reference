# Create Facility Address with Recreation.gov

Creates a facility address in Recreation.gov.

## Endpoint

- **Method:** `POST`
- **Path:** `/facilities/{id}/facilityaddresses`
- **Base URL:** `https://ridb.recreation.gov/api/v1`
- **Official documentation:** [Create Facility Address](https://ridb.recreation.gov/shared/swagger/dataSteward.yaml)

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
