# Update Resource with Meisterplan

Updates an existing resource in Meisterplan.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/resources/:resourceId`
- **Base URL:** `https://api.us.meisterplan.com/v1`
- **Official documentation:** [Update Resource](https://api.us.meisterplan.com/docs/api.html#operation/UpdateResource)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `resourceId` | path | `string` | yes |
| `resourceKey` | body | `string` | no |
| `firstName` | body | `string` | no |
| `lastName` | body | `string` | no |
| `externalId` | body | `string` | no |
| `emailAddress` | body | `string` | no |
| `postalAddress` | body | `object` | no |
| `employmentPeriod` | body | `object` | no |
| `externalResource` | body | `boolean` | no |
| `primaryRole` | body | `object` | no |
| `calendar` | body | `object` | no |
| `obsUnits` | body | `object` | no |
| `skills[]` | body | `array<string>` | no |
| `resourceManager` | body | `object` | no |
| `costPerHour` | body | `number` | no |
| `costPerHourValidFrom` | body | `date` | no |
| `costRates[]` | body | `array<object>` | no |
