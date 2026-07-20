# Get Datasource with Microsoft Power BI

## Endpoint

- **Method:** `GET`
- **Path:** `gateways/[:gatewayId]/datasources/[:datasourceId]`
- **Base URL:** `https://api.powerbi.com/v1.0/myorg`
- **Official documentation:** [Get Datasource](https://learn.microsoft.com/en-us/rest/api/power-bi/gateways/get-datasource)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `gatewayId` | path | `string` | yes | The gateway ID. When using a gateway cluster, the gateway ID refers to the primary (first) gateway in the cluster. In such cases, gateway ID is similar to gateway cluster ID. |
| `datasourceId` | path | `string` | yes | The data source ID |
