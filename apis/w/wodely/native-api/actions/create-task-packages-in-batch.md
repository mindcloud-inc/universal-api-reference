# Create Task Packages in Batch with Wodely

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/taskPackages`
- **Base URL:** `https://api.wodely.com`
- **Official documentation:** [Create Task Packages in Batch](https://app.wodely.com/doc/api-documentation.html#create-task-packages)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `taskGuid` | body | `string` | yes | Task identifier returned by Wodely. |
| `deleteOldPackages` | body | `boolean` | no | Delete all existing packages on the task before adding the new ones. |
| `packages[].productId` | body | `string` | no | Product Id or item Id |
| `packages[].productDesc` | body | `string` | yes | Short description of the package item. |
| `packages[].orderId` | body | `string` | no | Order Id |
| `packages[].quantity` | body | `number` | no | Quantity for each package line. |
| `packages[].weight` | body | `number` | no | Weight for each package line. |
| `packages[].price` | body | `number` | no | Price or line total for each package line. |
| `packages[].packageTypeId` | body | `number` | no | Package type identifier. |
| `packages[].labelId` | body | `string` | no | Label or barcode |
| `packages[].field1` | body | `string` | no | Custom Field 1 |
| `packages[].field2` | body | `string` | no | Custom Field 2 |
| `packages[].field3` | body | `string` | no | Custom Field 3 |
| `packages[].field4` | body | `string` | no | Custom Field 4 |
| `packages[].field5` | body | `string` | no | Custom Field 5 |
