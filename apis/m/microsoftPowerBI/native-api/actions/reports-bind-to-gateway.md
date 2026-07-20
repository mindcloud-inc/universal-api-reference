# Bind To Gateway with Microsoft Power BI

## Endpoint

- **Method:** `POST`
- **Path:** `reports/[:reportId]/Default.BindToGateway`
- **Base URL:** `https://api.powerbi.com/v1.0/myorg`
- **Official documentation:** [Bind To Gateway](https://learn.microsoft.com/en-us/rest/api/power-bi/reports/bind-to-gateway)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `reportId` | path | `string` | yes | The report ID |
| `bindDetails[]` | body | `array<object>` | yes | List of bind details |
| `gatewayObjectId` | body | `string` | yes | The gateway ID. When using a gateway cluster, the gateway ID refers to the primary (first) gateway in the cluster and is similar to the gateway cluster ID. |
