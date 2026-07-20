# Profiles GetProfilesAsAdmin with Microsoft Power BI

## Endpoint

- **Method:** `GET`
- **Path:** `admin/profiles`
- **Base URL:** `https://api.powerbi.com/v1.0/myorg`
- **Official documentation:** [Profiles GetProfilesAsAdmin](https://learn.microsoft.com/en-us/rest/api/power-bi/admin/profiles-get-profiles-as-admin)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `$filter` | query | `string` | no | Filters the results based on a boolean condition, using 'id', 'displayName', or 'servicePrincipalId'. Supports only 'eq' operator. |
| `$skip` | query | `number` | no | Skips the first n results. Use with top to fetch results beyond the first 5000. |
| `$top` | query | `number` | no | Returns only the first n results. This parameter must be in the range of 1-5000. |
