# Get Occurrence with Rollbar

Retrieves an occurrence from Rollbar.

## Endpoint

- **Method:** `GET`
- **Path:** `/instance/:instanceId`
- **Base URL:** `https://api.rollbar.com/api/1`
- **Official documentation:** [Get Occurrence](https://docs.rollbar.com/reference/get_api-1-instance-instance-id)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `instanceId` | path | `number` | yes | Rollbar occurrence identifier. |
