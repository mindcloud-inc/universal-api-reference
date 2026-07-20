# Dataflows GetDataflowsInGroupAsAdmin with Microsoft Power BI

## Endpoint

- **Method:** `GET`
- **Path:** `admin/groups/[:groupId]/dataflows`
- **Base URL:** `https://api.powerbi.com/v1.0/myorg`
- **Official documentation:** [Dataflows GetDataflowsInGroupAsAdmin](https://learn.microsoft.com/en-us/rest/api/power-bi/admin/dataflows-get-dataflows-in-group-as-admin)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `groupId` | path | `string` | yes | The workspace ID |
| `$filter` | query | `string` | no | Returns a subset of a results based on Odata filter query parameter condition. |
| `$skip` | query | `number` | no | Skips the first n results |
| `$top` | query | `number` | no | Returns only the first n results |
