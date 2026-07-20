# Dataflows GetUpstreamDataflowsInGroupAsAdmin with Microsoft Power BI

## Endpoint

- **Method:** `GET`
- **Path:** `admin/groups/[:groupId]/dataflows/[:dataflowId]/upstreamDataflows`
- **Base URL:** `https://api.powerbi.com/v1.0/myorg`
- **Official documentation:** [Dataflows GetUpstreamDataflowsInGroupAsAdmin](https://learn.microsoft.com/en-us/rest/api/power-bi/admin/dataflows-get-upstream-dataflows-in-group-as-admin)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `groupId` | path | `string` | yes | The workspace ID |
| `dataflowId` | path | `string` | yes | The dataflow ID |
