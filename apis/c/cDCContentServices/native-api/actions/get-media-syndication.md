# Get Media Syndication with CDC Content Services

Retrieves media syndication details from CDC Content Services.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/resources/media/[:mediaId]/syndicate`
- **Base URL:** `https://tools.cdc.gov/api`
- **Official documentation:** [Get Media Syndication](https://tools.cdc.gov/api/docs/info.aspx)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `mediaId` | path | `number` | yes | CDC media identifier. |
| `stripScripts` | query | `boolean` | no | When true, JavaScript is stripped from syndicated results. CDC defaults to true. |
| `stripImages` | query | `boolean` | no | When true, images are stripped from syndicated results. |
