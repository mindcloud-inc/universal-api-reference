# Update Company with Productlane

Updates an existing company in Productlane.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/companies/:id`
- **Base URL:** `https://productlane.com/api/v1`
- **Official documentation:** [Update Company](https://productlane.mintlify.dev/docs/api/companies/update-company)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string` | yes |
| `name` | body | `string` | no |
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
