# Run Spider with ScrapeOps

Runs a spider on a ScrapeOps server.

## Endpoint

- **Method:** `POST`
- **Path:** `https://backend.scrapeops.io/v1/client/spiders/run`
- **Base URL:** `http://headers.scrapeops.io/v1`
- **Official documentation:** [Run Spider](https://scrapeops.io/docs/servers-scheduling/rest-api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `serverId` | body | `number` | yes | The numeric ScrapeOps server id that owns the spider. |
| `selectedSpiderId` | body | `number` | yes | The numeric spider id to run on the selected server. |
