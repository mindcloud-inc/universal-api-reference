# Get Survey Statistics with SatisMeter

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v3/projects/:projectId/campaigns/:campaignId/statistics`
- **Base URL:** `https://app.satismeter.com`
- **Official documentation:** [Get Survey Statistics](https://app.satismeter.com/apidoc#tag/Statistics/paths/~1projects~1{projectId}~1campaigns~1{campaignId}~1statistics/get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `campaignId` | path | `string` | yes | Survey ID. |
| `endDate` | query | `date` | no | Filter statistics using responses recorded before this ISO 8601 timestamp. |
| `projectId` | path | `string` | yes | Project ID. |
| `startDate` | query | `date` | no | Filter statistics using responses recorded after this ISO 8601 timestamp. |
