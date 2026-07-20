# Create Service with Kiwili

Creates a new service in Kiwili.

## Endpoint

- **Method:** `POST`
- **Path:** `/service`
- **Base URL:** `https://mindcloud.kiwili.com/api`
- **Official documentation:** [Create Service](https://api.kiwili.com/api/openapi/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Active` | body | `boolean` | no | Whether the service is active. |
| `Billable` | body | `boolean` | no | Whether the service is billable. |
| `Name` | body | `string` | yes | The service name. |
| `Rate` | body | `number` | yes | The hourly or fixed rate for the service. |
