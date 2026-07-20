# List Speaker Wall with Sessionize

Retrieves speaker wall profiles from Sessionize.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/:endpointId/view/SpeakerWall`
- **Base URL:** `https://sessionize.com`
- **Official documentation:** [List Speaker Wall](https://sessionize.com/playbook/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `endpointId` | path | `string` | yes | Sessionize event API endpoint ID from URLs like https://sessionize.com/api/v2/{endpointId}/view/SpeakerWall. |
