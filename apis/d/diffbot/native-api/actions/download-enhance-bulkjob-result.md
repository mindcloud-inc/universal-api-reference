# Download Enhance Bulkjob Result with Diffbot

Downloads a single result from a Diffbot Enhance bulk job.

## Endpoint

- **Method:** `GET`
- **Path:** `https://kg.diffbot.com/kg/v3/enhance/bulk/{bulkjobId}/{jobIdx}`
- **Base URL:** `https://api.diffbot.com`
- **Official documentation:** [Download Enhance Bulkjob Result](https://docs.diffbot.com/reference/download-single-result-of-bulkjob)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `bulkjobId` | path | `string` | yes | Enhance bulkjob identifier. |
| `jobIdx` | path | `string` | yes | Result index inside the enhance bulkjob. |
