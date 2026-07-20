# Update Profile with Microsoft Power BI

## Endpoint

- **Method:** `PUT`
- **Path:** `profiles/[:profileId]`
- **Base URL:** `https://api.powerbi.com/v1.0/myorg`
- **Official documentation:** [Update Profile](https://learn.microsoft.com/en-us/rest/api/power-bi/profiles/update-profile)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `profileId` | path | `string` | yes | The service principal profile ID |
| `displayName` | body | `string` | no | The service principal profile name |
