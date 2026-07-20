# List Spiders By Server Id with ScrapeOps

Retrieves spiders for a ScrapeOps server.

## Endpoint

- **Method:** `GET`
- **Path:** `https://backend.scrapeops.io/v1/client/servers/:serverId/spiders`
- **Base URL:** `http://headers.scrapeops.io/v1`
- **Official documentation:** [List Spiders By Server Id](https://scrapeops.io/docs/servers-scheduling/rest-api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `serverId` | path | `number` | yes | The numeric ScrapeOps server id whose spiders you want to list. |
