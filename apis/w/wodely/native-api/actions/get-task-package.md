# Get Task Package with Wodely

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/taskPackages/[:packageId]`
- **Base URL:** `https://api.wodely.com`
- **Official documentation:** [Get Task Package](https://app.wodely.com/doc/api-documentation.html#get-task-package)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `packageId` | path | `number` | yes | Package identifier returned by Wodely. |
| `taskGuid` | body | `string` | yes | Task identifier for the package. |
