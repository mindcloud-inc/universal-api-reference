# List Session Groups with Sessionize

Retrieves grouped event sessions from Sessionize.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/:endpointId/view/Sessions`
- **Base URL:** `https://sessionize.com`
- **Official documentation:** [List Session Groups](https://sessionize.com/playbook/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `endpointId` | path | `string` | yes | Sessionize event API endpoint ID from URLs like https://sessionize.com/api/v2/{endpointId}/view/Sessions. |
