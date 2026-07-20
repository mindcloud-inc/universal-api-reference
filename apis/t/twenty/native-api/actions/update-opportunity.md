# Update Opportunity with Twenty

## Endpoint

- **Method:** `PATCH`
- **Path:** `/rest/opportunities/:id`
- **Base URL:** `https://api.twenty.com`
- **Official documentation:** [Update Opportunity](https://docs.twenty.com/developers/extend/api)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string` | yes |
| `closeDate` | body | `date` | no |
| `amount.amountMicros` | body | `number` | no |
| `amount.currencyCode` | body | `string` | no |
| `stage` | body | `string` | no |
| `name` | body | `string` | no |
| `companyId` | body | `string` | no |
| `pointOfContactId` | body | `string` | no |
| `ownerId` | body | `string` | no |
