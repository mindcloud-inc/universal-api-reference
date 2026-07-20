# Create Company with Productlane

Creates a new company in Productlane.

## Endpoint

- **Method:** `POST`
- **Path:** `/companies`
- **Base URL:** `https://productlane.com/api/v1`
- **Official documentation:** [Create Company](https://productlane.mintlify.dev/docs/api/companies/create-company)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `name` | body | `string` | yes |
| `domains[]` | body | `array<string>` | no |
| `autoAdd` | body | `boolean` | no |
| `externalIds[]` | body | `array<string>` | no |
| `size` | body | `number` | no |
| `revenue` | body | `number` | no |
| `tierId` | body | `string` | no |
| `tierName` | body | `string` | no |
| `statusId` | body | `string` | no |
| `statusName` | body | `string` | no |
| `statusColor` | body | `string` | no |
