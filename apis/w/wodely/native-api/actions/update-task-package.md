# Update Task Package with Wodely

## Endpoint

- **Method:** `PUT`
- **Path:** `/v2/taskPackages/[:packageId]`
- **Base URL:** `https://api.wodely.com`
- **Official documentation:** [Update Task Package](https://app.wodely.com/doc/api-documentation.html#update-task-package)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `packageId` | path | `number` | yes | Package identifier returned by Wodely. |
| `taskGuid` | body | `string` | yes | Task identifier for the package. |
| `productId` | body | `string` | no | Product Id or item Id |
| `productDesc` | body | `string` | no | Short description of the item |
| `orderId` | body | `string` | no | Order Id |
| `quantity` | body | `number` | no | Shipping Quantity |
| `weight` | body | `number` | no | Total Weight |
| `price` | body | `number` | no | Line Total |
| `packageTypeId` | body | `number` | no | Package type Id |
| `labelId` | body | `string` | no | Label or barcode |
| `field1` | body | `string` | no | Custom Field 1 |
| `field2` | body | `string` | no | Custom Field 2 |
| `field3` | body | `string` | no | Custom Field 3 |
| `field4` | body | `string` | no | Custom Field 4 |
| `field5` | body | `string` | no | Custom Field 5 |
