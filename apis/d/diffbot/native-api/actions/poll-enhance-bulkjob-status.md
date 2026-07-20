# Poll Enhance Bulkjob Status with Diffbot

Retrieves the status of a Diffbot Enhance bulk job.

## Endpoint

- **Method:** `GET`
- **Path:** `https://kg.diffbot.com/kg/v3/enhance/bulk/{bulkjobId}/status`
- **Base URL:** `https://api.diffbot.com`
- **Official documentation:** [Poll Enhance Bulkjob Status](https://docs.diffbot.com/reference/poll-bulkjob-status)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `bulkjobId` | path | `string` | yes | Enhance bulkjob identifier. |
