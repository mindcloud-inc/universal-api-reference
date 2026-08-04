# Create Opportunity with Autotask

## Endpoint

- **Method:** `POST`
- **Path:** `/Opportunities`
- **Base URL:** `https://webservices14.autotask.net/ATServicesRest/v1.0`
- **Official documentation:** [Create Opportunity](https://autotask.net/help/developerhelp/content/apis/rest/entities/OpportunitiesEntity.htm)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `amount` | body | `number` | yes |
| `companyID` | body | `number` | yes |
| `cost` | body | `number` | yes |
| `ownerResourceID` | body | `number` | yes |
| `probability` | body | `number` | yes |
| `projectedCloseDate` | body | `date` | yes |
| `stage` | body | `number` | yes |
| `startDate` | body | `date` | yes |
| `status` | body | `number` | yes |
| `title` | body | `string` | yes |
| `useQuoteTotals` | body | `boolean` | yes |
| `contactID` | body | `number` | no |
| `description` | body | `string` | no |
| `opportunityCategoryID` | body | `number` | no |
| `nextStep` | body | `string` | no |
