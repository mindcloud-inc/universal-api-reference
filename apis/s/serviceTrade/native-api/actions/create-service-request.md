# Create Service Request with ServiceTrade

Creates a new service request in ServiceTrade.

## Endpoint

- **Method:** `POST`
- **Path:** `servicerequest`
- **Base URL:** `https://api.servicetrade.com/api`
- **Official documentation:** [Create Service Request](https://api.servicetrade.com/api/docs#resource-servicerequest)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `locationId` | body | `number` | yes | Location where the service request is created. |
| `serviceLineId` | body | `number` | yes | Service line for the requested work. |
| `description` | body | `string` | yes | Description of the service requested. |
