# Delete Occurrence with Rollbar

Deletes an existing occurrence from Rollbar.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/instance/:instanceId`
- **Base URL:** `https://api.rollbar.com/api/1`
- **Official documentation:** [Delete Occurrence](https://docs.rollbar.com/reference/delete_api-1-instance-instance-id)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `instanceId` | path | `number` | yes | Rollbar occurrence identifier. |
