# Bind To Gateway with Microsoft Power BI

## Endpoint

- **Method:** `POST`
- **Path:** `datasets/[:datasetId]/Default.BindToGateway`
- **Base URL:** `https://api.powerbi.com/v1.0/myorg`
- **Official documentation:** [Bind To Gateway](https://learn.microsoft.com/en-us/rest/api/power-bi/datasets/bind-to-gateway)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `datasetId` | path | `string` | yes | The dataset ID |
| `gatewayObjectId` | body | `string` | yes | The gateway ID. When using a gateway cluster, the gateway ID refers to the primary (first) gateway in the cluster and is similar to the gateway cluster ID. |
| `datasourceObjectIds[]` | body | `array<string>` | no | The unique identifiers for the data sources in the gateway |
