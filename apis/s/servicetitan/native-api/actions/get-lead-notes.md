# Get Lead Notes with ServiceTitan

Retrieves lead notes from ServiceTitan.

## Endpoint

- **Method:** `GET`
- **Path:** `crm/v2/tenant/{tenant}/leads/:leadId/notes`
- **Base URL:** `https://{baseUrl}/`
- **Official documentation:** [Get Lead Notes](https://developer.servicetitan.io/api-details/#api=tenant-crm-v2&operation=Leads_GetNotes)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `leadId` | path | `string` | yes |
| `createdBefore` | query | `string` | no |
| `createdOnOrAfter` | query | `string` | no |
| `modifiedBefore` | query | `string` | no |
| `modifiedOnOrAfter` | query | `string` | no |
