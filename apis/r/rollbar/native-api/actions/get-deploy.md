# Get Deploy with Rollbar

Retrieves a deploy from Rollbar.

## Endpoint

- **Method:** `GET`
- **Path:** `/deploy/:deployId`
- **Base URL:** `https://api.rollbar.com/api/1`
- **Official documentation:** [Get Deploy](https://docs.rollbar.com/reference/get-a-deploy)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `deployId` | path | `number` | yes | Rollbar deploy identifier. |
