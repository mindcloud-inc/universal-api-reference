# Get Campaign Statistics with ManyReach

Retrieves campaign statistics from ManyReach.

## Endpoint

- **Method:** `GET`
- **Path:** `https://api.manyreach.com/api/v2/campaigns/:id/stats`
- **Base URL:** `https://api.manyreach.com`
- **Official documentation:** [Get Campaign Statistics](https://api.manyreach.com/api#v2/tag/campaign)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Campaign ID for which statistics are retrieved. |
| `dateStart` | query | `date` | no | Start date for the statistics range. |
| `dateEnd` | query | `date` | no | End date for the statistics range. |
| `refresh` | query | `boolean` | no | Force-refresh campaign statistics before retrieval. |
