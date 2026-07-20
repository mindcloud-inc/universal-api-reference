# Create Scheduled Job with ScrapeOps

Creates a scheduled job in ScrapeOps.

## Endpoint

- **Method:** `POST`
- **Path:** `https://backend.scrapeops.io/v1/client/scheduled-jobs`
- **Base URL:** `http://headers.scrapeops.io/v1`
- **Official documentation:** [Create Scheduled Job](https://scrapeops.io/docs/servers-scheduling/rest-api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `serverId` | body | `number` | yes | The numeric ScrapeOps server id that owns the scheduled spider. |
| `serverSpiderId` | body | `number` | yes | The numeric spider id to schedule on the selected server. |
| `cronToken` | body | `string` | yes | The cron expression that controls when the job runs. |
