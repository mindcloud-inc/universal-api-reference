# Bind To Gateway In Group with Microsoft Power BI

## Endpoint

- **Method:** `POST`
- **Path:** `groups/[:groupId]/reports/[:reportId]/Default.BindToGateway`
- **Base URL:** `https://api.powerbi.com/v1.0/myorg`
- **Official documentation:** [Bind To Gateway In Group](https://learn.microsoft.com/en-us/rest/api/power-bi/reports/bind-to-gateway-in-group)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `groupId` | path | `string` | yes | The workspace ID |
| `reportId` | path | `string` | yes | The report ID |
| `bindDetails[]` | body | `array<object>` | yes | List of bind details |
| `gatewayObjectId` | body | `string` | yes | The gateway ID. When using a gateway cluster, the gateway ID refers to the primary (first) gateway in the cluster and is similar to the gateway cluster ID. |
