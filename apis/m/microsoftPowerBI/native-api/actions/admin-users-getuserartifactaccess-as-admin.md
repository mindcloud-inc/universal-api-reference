# Users GetUserArtifactAccessAsAdmin with Microsoft Power BI

## Endpoint

- **Method:** `GET`
- **Path:** `admin/users/[:userId]/artifactAccess`
- **Base URL:** `https://api.powerbi.com/v1.0/myorg`
- **Official documentation:** [Users GetUserArtifactAccessAsAdmin](https://learn.microsoft.com/en-us/rest/api/power-bi/admin/users-get-user-artifact-access-as-admin)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `userId` | path | `string` | yes | The graph ID or user principal name (UPN) of the user |
| `artifactTypes` | query | `string` | no | Comma separated list of artifact types. |
| `continuationToken` | query | `string` | no | Token required to get the next chunk of the result set |
