# Get Media Content with CDC Content Services

Retrieves media content from CDC Content Services.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/resources/media/[:mediaId]/content`
- **Base URL:** `https://tools.cdc.gov/api`
- **Official documentation:** [Get Media Content](https://tools.cdc.gov/api/docs/info.aspx)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `mediaId` | path | `number` | yes | CDC media identifier. |
| `stripScripts` | query | `boolean` | no | When true, JavaScript is stripped from content results. CDC defaults to true. |
