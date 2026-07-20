# Update Workspace Avatar with Kite Suite

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/v1/workspace/avatar/:id`
- **Base URL:** `https://api.kitesuite.com`
- **Official documentation:** [Update Workspace Avatar](https://api.kitesuite.com/swagger/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `avatar` | body | `string` | yes | The avatar image file. |
| `body` | body | `object` | yes | Request body |
| `id` | path | `string` | yes | workspace ID |
