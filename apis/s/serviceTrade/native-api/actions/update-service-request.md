# Update Service Request with ServiceTrade

Updates an existing service request in ServiceTrade.

## Endpoint

- **Method:** `PUT`
- **Path:** `servicerequest/:serviceRequestId`
- **Base URL:** `https://api.servicetrade.com/api`
- **Official documentation:** [Update Service Request](https://api.servicetrade.com/api/docs#resource-servicerequest)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `serviceRequestId` | path | `number` | yes | Service request to update. |
| `description` | body | `string` | no | Updated service request description. |
| `status` | body | `string` | no | Updated service request status. |
