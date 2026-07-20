# Update Monitor with Postman

Updates an existing monitor in Postman.

## Endpoint

- **Method:** `PUT`
- **Path:** `/monitors/:monitorId`
- **Base URL:** `https://api.getpostman.com`
- **Official documentation:** [Update Monitor](https://www.postman.com/postman/postman-public-workspace/request/xbdpc2a/update-a-monitor)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `monitorId` | path | `string` | yes | The monitor's ID. |
| `monitor.name` | body | `string` | no | — |
