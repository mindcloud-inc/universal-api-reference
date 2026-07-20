# Update Deploy with Rollbar

Updates an existing deploy in Rollbar.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/deploy/:deployId`
- **Base URL:** `https://api.rollbar.com/api/1`
- **Official documentation:** [Update Deploy](https://docs.rollbar.com/reference/update-a-deploy)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `deployId` | path | `number` | yes | Rollbar deploy identifier. |
