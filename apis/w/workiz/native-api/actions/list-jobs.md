# List Jobs with Workiz

Finds jobs in Workiz by filter criteria.

## Endpoint

- **Method:** `GET`
- **Path:** `/job/all/`
- **Base URL:** `https://api.workiz.com/api/v1/{apiKey}`
- **Official documentation:** [List Jobs](https://developer.workiz.com/#/Jobs/getJobs)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `only_open` | query | `boolean` | no | Only list open jobs, excluding done and canceled statuses. |
| `start_date` | query | `string` | no | The date range start in yyyy-MM-dd format. |
| `status[]` | query | `array<string>` | no | Array of statuses to list. |
