# Groups GetUnusedArtifactsAsAdmin with Microsoft Power BI

## Endpoint

- **Method:** `GET`
- **Path:** `admin/groups/[:groupId]/unused`
- **Base URL:** `https://api.powerbi.com/v1.0/myorg`
- **Official documentation:** [Groups GetUnusedArtifactsAsAdmin](https://learn.microsoft.com/en-us/rest/api/power-bi/admin/groups-get-unused-artifacts-as-admin)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `groupId` | path | `string` | yes | The workspace ID |
| `continuationToken` | query | `string` | no | Token required to get the next chunk of the result set |
