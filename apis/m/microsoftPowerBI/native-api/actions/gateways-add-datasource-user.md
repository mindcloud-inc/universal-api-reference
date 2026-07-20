# Add Datasource User with Microsoft Power BI

## Endpoint

- **Method:** `POST`
- **Path:** `gateways/[:gatewayId]/datasources/[:datasourceId]/users`
- **Base URL:** `https://api.powerbi.com/v1.0/myorg`
- **Official documentation:** [Add Datasource User](https://learn.microsoft.com/en-us/rest/api/power-bi/gateways/add-datasource-user)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `gatewayId` | path | `string` | yes | The gateway ID. When using a gateway cluster, the gateway ID refers to the primary (first) gateway in the cluster. In such cases, gateway ID is similar to gateway cluster ID. |
| `datasourceId` | path | `string` | yes | The data source ID |
| `datasourceAccessRight` | body | `object` | yes | The access right (permission level) that a user has on the data source |
| `displayName` | body | `string` | no | The display name of the principal |
| `emailAddress` | body | `string` | no | The email address of the user |
| `identifier` | body | `string` | no | The object ID of the principal |
| `principalType` | body | `list` | no | The principal type |
| `profile` | body | `object` | no | A Power BI service principal profile. Only relevant for Power BI Embedded multi-tenancy solution. |
