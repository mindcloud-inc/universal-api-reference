# Download Screenshot with ScrapFly

Retrieves a screenshot attachment from ScrapFly.

## Endpoint

- **Method:** `GET`
- **Path:** `/screenshot/:screenshotId/main`
- **Base URL:** `https://api.scrapfly.io`
- **Official documentation:** [Download Screenshot](https://scrapfly.io/docs/screenshot-api/getting-started)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `screenshotId` | path | `string` | yes | Screenshot identifier returned by ScrapFly. |
