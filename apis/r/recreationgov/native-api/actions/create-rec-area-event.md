# Create Rec Area Event with Recreation.gov

Creates a recreation area event in Recreation.gov.

## Endpoint

- **Method:** `POST`
- **Path:** `/recareas/{id}/events`
- **Base URL:** `https://ridb.recreation.gov/api/v1`
- **Official documentation:** [Create Rec Area Event](https://ridb.recreation.gov/shared/swagger/dataSteward.yaml)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `number` | yes |
| `name` | body | `string` | yes |
| `description` | body | `string` | no |
| `typeDescription` | body | `string` | no |
| `scopeDescription` | body | `string` | no |
| `frequencyRateDescription` | body | `string` | no |
| `feeDescription` | body | `string` | no |
| `ageGroup` | body | `string` | no |
| `registrationRequired` | body | `boolean` | no |
| `adaAccess` | body | `string` | no |
| `comments` | body | `string` | no |
| `email` | body | `string` | no |
| `url` | body | `string` | no |
| `urlText` | body | `string` | no |
| `startDate` | body | `date` | no |
| `endDate` | body | `date` | no |
| `sponsorName` | body | `string` | no |
| `sponsorClassType` | body | `string` | no |
| `sponsorPhone` | body | `string` | no |
| `sponsorEmail` | body | `string` | no |
| `sponsorUrl` | body | `string` | no |
| `sponsorUrlText` | body | `string` | no |
