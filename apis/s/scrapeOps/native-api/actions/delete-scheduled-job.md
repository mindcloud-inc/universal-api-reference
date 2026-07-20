# Delete Scheduled Job with ScrapeOps

Deletes a scheduled job from ScrapeOps.

## Endpoint

- **Method:** `DELETE`
- **Path:** `https://backend.scrapeops.io/v1/client/scheduled-jobs/:jobId`
- **Base URL:** `http://headers.scrapeops.io/v1`
- **Official documentation:** [Delete Scheduled Job](https://scrapeops.io/docs/servers-scheduling/rest-api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `jobId` | path | `number` | yes | The numeric scheduled job id to delete. |
