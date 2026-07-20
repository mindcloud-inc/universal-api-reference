# List Schedule Days with Sessionize

Retrieves event schedule days from Sessionize.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/:endpointId/view/GridSmart`
- **Base URL:** `https://sessionize.com`
- **Official documentation:** [List Schedule Days](https://sessionize.com/playbook/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `endpointId` | path | `string` | yes | Sessionize event API endpoint ID from URLs like https://sessionize.com/api/v2/{endpointId}/view/GridSmart. |
