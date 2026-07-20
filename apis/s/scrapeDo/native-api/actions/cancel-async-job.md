# Cancel async job with Scrape do

Cancels an async job in Scrape do.

## Endpoint

- **Method:** `DELETE`
- **Path:** `https://q.scrape.do/api/v1/jobs/:jobID`
- **Base URL:** `https://api.scrape.do`
- **Official documentation:** [Cancel async job](https://scrape.do/documentation/async-api/cancel-job/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `jobID` | path | `string` | yes | The async job identifier to cancel. |
