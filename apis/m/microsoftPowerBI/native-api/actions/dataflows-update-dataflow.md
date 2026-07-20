# Update Dataflow with Microsoft Power BI

## Endpoint

- **Method:** `PATCH`
- **Path:** `groups/[:groupId]/dataflows/[:dataflowId]`
- **Base URL:** `https://api.powerbi.com/v1.0/myorg`
- **Official documentation:** [Update Dataflow](https://learn.microsoft.com/en-us/rest/api/power-bi/dataflows/update-dataflow)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `groupId` | path | `string` | yes | The workspace ID |
| `dataflowId` | path | `string` | yes | The dataflow ID |
| `allowNativeQueries` | body | `boolean` | no | Whether to allow native queries |
| `computeEngineBehavior` | body | `object` | no | The behavior of the compute engine |
| `description` | body | `string` | no | The new description for the dataflow |
| `name` | body | `string` | no | The new name for the dataflow |
