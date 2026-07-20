# Create Datasource with Microsoft Power BI

## Endpoint

- **Method:** `POST`
- **Path:** `gateways/[:gatewayId]/datasources`
- **Base URL:** `https://api.powerbi.com/v1.0/myorg`
- **Official documentation:** [Create Datasource](https://learn.microsoft.com/en-us/rest/api/power-bi/gateways/create-datasource)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `gatewayId` | path | `string` | yes | The gateway ID. When using a gateway cluster, the gateway ID refers to the primary (first) gateway in the cluster. In such cases, gateway ID is similar to gateway cluster ID. |
| `connectionDetails` | body | `string` | yes | The connection details |
| `credentialDetails` | body | `object` | yes | The credential details |
| `dataSourceName` | body | `string` | yes | The data source name |
| `dataSourceType` | body | `string` | yes | The data source type |
