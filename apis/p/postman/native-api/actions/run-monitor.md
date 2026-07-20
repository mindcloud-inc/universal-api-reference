# Run Monitor with Postman

Runs an existing monitor in Postman.

## Endpoint

- **Method:** `POST`
- **Path:** `/monitors/:monitorId/run`
- **Base URL:** `https://api.getpostman.com`
- **Official documentation:** [Run Monitor](https://www.postman.com/postman/postman-public-workspace/request/80oupaf/run-a-monitor)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `monitorId` | path | `string` | yes | The monitor's ID. |
