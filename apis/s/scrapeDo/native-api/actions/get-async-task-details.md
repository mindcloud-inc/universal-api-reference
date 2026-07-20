# Get async task details with Scrape do

Retrieves async task details from Scrape do.

## Endpoint

- **Method:** `GET`
- **Path:** `https://q.scrape.do/api/v1/jobs/:jobID/:taskID`
- **Base URL:** `https://api.scrape.do`
- **Official documentation:** [Get async task details](https://scrape.do/documentation/async-api/get-task/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `jobID` | path | `string` | yes | The async job identifier. |
| `taskID` | path | `string` | yes | The async task identifier. |
