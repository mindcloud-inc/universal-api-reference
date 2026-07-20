# Get Campaign Stats with LinkedCamp

## Endpoint

- **Method:** `GET`
- **Path:** `/campaigns/:campaignId/stats`
- **Base URL:** `https://api.linkedcamp.com`
- **Official documentation:** [Get Campaign Stats](https://api.linkedcamp.com/docs/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `campaignId` | path | `string` | yes | Campaign identifier. |
| `userId` | query | `string` | no | Optional user identifier for stats. |
| `range` | query | `string` | no | Optional date range for stats. |
