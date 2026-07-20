# List Purchase Orders with Logiwa Legacy WMS

By using this endpoint, the users can obtain the list of all the purchase orders based on the entered criteria.

## Endpoint

- **Method:** `POST`
- **Path:** `en/api/IntegrationApi/PurchaseOrderSearch`
- **Base URL:** `https://{uRL}.logiwa.com/`
- **Official documentation:** [List Purchase Orders](https://developer.logiwa.com/?id=5df0dbf9e6466c2eec992f5d)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Code` | path | `string` | no | Purchase order code |
