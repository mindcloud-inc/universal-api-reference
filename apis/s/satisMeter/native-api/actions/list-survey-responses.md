# List Survey Responses with SatisMeter

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v3/projects/:projectId/campaigns/:campaignId/responses`
- **Base URL:** `https://app.satismeter.com`
- **Official documentation:** [List Survey Responses](https://app.satismeter.com/apidoc#tag/Responses/paths/~1projects~1{projectId}~1campaigns~1{campaignId}~1responses/get)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `campaignId` | path | `string` | yes | Survey ID. |
| `endDate` | query | `date` | no | Filter responses recorded before this ISO 8601 timestamp. |
| `projectId` | path | `string` | yes | Project ID. |
| `startDate` | query | `date` | no | Filter responses recorded after this ISO 8601 timestamp. |
