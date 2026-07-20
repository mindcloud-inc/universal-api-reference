# List Experience Availability Statistics with Bokun

Retrieves availability statistics for an experience product from Bokun.

## Endpoint

- **Method:** `GET`
- **Path:** `/restapi/v2.0/availability/:experienceId/statistics`
- **Base URL:** `https://api.bokun.io`
- **Official documentation:** [List Experience Availability Statistics](https://api-docs.bokun.dev/rest-v2.yaml)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `experienceId` | path | `number` | yes | The Bokun experience ID. |
| `from` | query | `string` | yes | The start date in yyyy-MM-dd format. |
| `to` | query | `string` | yes | The end date in yyyy-MM-dd format. |
