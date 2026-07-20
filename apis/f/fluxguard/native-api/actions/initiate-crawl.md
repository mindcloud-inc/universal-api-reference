# Initiate Crawl with Fluxguard

Initiates a crawl for a Fluxguard monitoring session.

## Endpoint

- **Method:** `POST`
- **Path:** `/site/:siteId/session/:sessionId/crawl`
- **Base URL:** `https://api.fluxguard.com`
- **Official documentation:** [Initiate Crawl](https://fluxguard.com/how-to-guides/use-our-api/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `siteId` | path | `string` | yes |
| `sessionId` | path | `string` | yes |
