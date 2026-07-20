# Get Profiles with Microsoft Power BI

## Endpoint

- **Method:** `GET`
- **Path:** `profiles`
- **Base URL:** `https://api.powerbi.com/v1.0/myorg`
- **Official documentation:** [Get Profiles](https://learn.microsoft.com/en-us/rest/api/power-bi/profiles/get-profiles)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `$filter` | query | `string` | no | Get a profile by DisplayName |
| `$skip` | query | `number` | no | Skips the first n results |
| `$top` | query | `number` | no | Returns only the first n results |
