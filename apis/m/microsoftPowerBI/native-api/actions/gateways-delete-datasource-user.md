# Delete Datasource User with Microsoft Power BI

## Endpoint

- **Method:** `DELETE`
- **Path:** `gateways/[:gatewayId]/datasources/[:datasourceId]/users/[:emailAdress]`
- **Base URL:** `https://api.powerbi.com/v1.0/myorg`
- **Official documentation:** [Delete Datasource User](https://learn.microsoft.com/en-us/rest/api/power-bi/gateways/delete-datasource-user)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `gatewayId` | path | `string` | yes | The gateway ID. When using a gateway cluster, the gateway ID refers to the primary (first) gateway in the cluster. In such cases, gateway ID is similar to gateway cluster ID. |
| `datasourceId` | path | `string` | yes | The data source ID |
| `emailAdress` | path | `string` | yes | The user's email address or the object ID of the service principal |
| `profileId` | query | `string` | no | The service principal profile ID to delete |
