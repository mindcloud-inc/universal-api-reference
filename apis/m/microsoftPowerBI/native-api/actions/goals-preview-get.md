# Get with Microsoft Power BI

## Endpoint

- **Method:** `GET`
- **Path:** `groups/[:groupId]/scorecards([:scorecardId])/goals`
- **Base URL:** `https://api.powerbi.com/v1.0/myorg`
- **Official documentation:** [Get](https://learn.microsoft.com/en-us/rest/api/power-bi/goals(preview)/get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `groupId` | path | `string` | yes | The unique identifier of the workspace |
| `scorecardId` | path | `string` | yes | The unique identifier of the scorecard |
| `$expand` | query | `string` | no | Accepts a comma-separated list of data types, which will be expanded inline in the response. Supports goalValues and aggregations. |
| `$select` | query | `string` | no | Allows the clients to select specific properties from the server. |
