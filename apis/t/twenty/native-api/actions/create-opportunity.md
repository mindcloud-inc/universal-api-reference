# Create Opportunity with Twenty

## Endpoint

- **Method:** `POST`
- **Path:** `/rest/opportunities`
- **Base URL:** `https://api.twenty.com`
- **Official documentation:** [Create Opportunity](https://docs.twenty.com/developers/extend/api)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `closeDate` | body | `date` | no |
| `amount.amountMicros` | body | `number` | no |
| `amount.currencyCode` | body | `string` | no |
| `stage` | body | `string` | yes |
| `name` | body | `string` | no |
| `companyId` | body | `string` | no |
| `pointOfContactId` | body | `string` | no |
| `ownerId` | body | `string` | no |
