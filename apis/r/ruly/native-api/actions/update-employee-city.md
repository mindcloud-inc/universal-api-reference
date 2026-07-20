# Update Employee City with Ruly

## Endpoint

- **Method:** `PUT`
- **Path:** `data/employee/:employeeId`
- **Base URL:** `https://mindcloud.api.rulyapp.com`
- **Official documentation:** [Update Employee City](https://rulyapp.com/quick-tips-using-ruly-api-in-postman-video/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `city` | body | `string` | yes | Employee city value to update. |
| `employeeId` | path | `string` | yes | Employee record identifier from the path. |
