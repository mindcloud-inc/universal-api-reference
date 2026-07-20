# Update Datasource with Microsoft Power BI

## Endpoint

- **Method:** `PATCH`
- **Path:** `gateways/[:gatewayId]/datasources/[:datasourceId]`
- **Base URL:** `https://api.powerbi.com/v1.0/myorg`
- **Official documentation:** [Update Datasource](https://learn.microsoft.com/en-us/rest/api/power-bi/gateways/update-datasource)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `gatewayId` | path | `string` | yes | The gateway ID. When using a gateway cluster, the gateway ID refers to the primary (first) gateway in the cluster. In such cases, gateway ID is similar to gateway cluster ID. |
| `datasourceId` | path | `string` | yes | The data source ID |
| `credentialDetails` | body | `object` | yes | The credential details |
