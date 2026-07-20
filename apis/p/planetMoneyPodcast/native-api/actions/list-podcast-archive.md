# List Podcast Archive with Planet Money Podcast

Retrieves older Planet Money episode listings from NPR.

## Endpoint

- **Method:** `GET`
- **Path:** `https://www.npr.org/podcasts/510289/planet-money/partials`
- **Base URL:** `https://feeds.npr.org/510289`
- **Official documentation:** [List Podcast Archive](https://www.npr.org/podcasts/510289/planet-money/partials?start=10)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `start` | query | `number` | no | Offset used by NPR's archive partials endpoint. Use larger values like 10, 20, or 30 to page deeper into older episodes. |
