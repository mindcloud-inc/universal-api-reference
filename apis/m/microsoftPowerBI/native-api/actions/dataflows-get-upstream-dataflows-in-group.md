# Get Upstream Dataflows In Group with Microsoft Power BI

## Endpoint

- **Method:** `GET`
- **Path:** `groups/[:groupId]/dataflows/[:dataflowId]/upstreamDataflows`
- **Base URL:** `https://api.powerbi.com/v1.0/myorg`
- **Official documentation:** [Get Upstream Dataflows In Group](https://learn.microsoft.com/en-us/rest/api/power-bi/dataflows/get-upstream-dataflows-in-group)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `groupId` | path | `string` | yes | The workspace ID |
| `dataflowId` | path | `string` | yes | The dataflow ID |
