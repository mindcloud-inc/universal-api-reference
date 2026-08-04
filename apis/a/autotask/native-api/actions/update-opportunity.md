# Update Opportunity with Autotask

## Endpoint

- **Method:** `PATCH`
- **Path:** `/Opportunities`
- **Base URL:** `https://webservices14.autotask.net/ATServicesRest/v1.0`
- **Official documentation:** [Update Opportunity](https://autotask.net/help/developerhelp/content/apis/rest/entities/OpportunitiesEntity.htm)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | body | `number` | yes |
| `title` | body | `string` | no |
| `description` | body | `string` | no |
| `status` | body | `number` | no |
| `stage` | body | `number` | no |
| `projectedCloseDate` | body | `date` | no |
| `ownerResourceID` | body | `number` | no |
| `probability` | body | `number` | no |
| `contactID` | body | `number` | no |
| `amount` | body | `number` | no |
| `cost` | body | `number` | no |
| `nextStep` | body | `string` | no |
| `closedDate` | body | `date` | no |
