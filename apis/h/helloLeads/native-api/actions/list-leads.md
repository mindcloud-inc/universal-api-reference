# List Leads with HelloLeads

## Endpoint

- **Method:** `GET`
- **Path:** `leadsOrderBy`
- **Base URL:** `https://app.helloleads.io/index.php/private/api`
- **Official documentation:** [List Leads](https://app.helloleads.io/index.php/app/account/layout#/apisettings)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `order` | query | `string` | no | Optional HelloLeads sort order string, for example desc as shown in the provider docs. |
| `createdDate` | query | `string` | no | Optional HelloLeads createdDate filter in provider format YYYY-MM-DD. This stays a string because HelloLeads expects the literal date string, not an ISO timestamp. |
