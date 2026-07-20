# Refresh Dataflow with Microsoft Power BI

## Endpoint

- **Method:** `POST`
- **Path:** `groups/[:groupId]/dataflows/[:dataflowId]/refreshes`
- **Base URL:** `https://api.powerbi.com/v1.0/myorg`
- **Official documentation:** [Refresh Dataflow](https://learn.microsoft.com/en-us/rest/api/power-bi/dataflows/refresh-dataflow)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `groupId` | path | `string` | yes | The workspace ID |
| `dataflowId` | path | `string` | yes | The dataflow ID |
| `processType` | query | `string` | no | Type of refresh process to use. |
| `notifyOption` | body | `object` | yes | Mail notification options |
