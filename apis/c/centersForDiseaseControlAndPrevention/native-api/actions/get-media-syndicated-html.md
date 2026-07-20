# Get Media Syndicated HTML with Centers for Disease Control and Prevention

Retrieves syndicated HTML for media from CDC Content Services.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/resources/media/:mediaId/syndicate`
- **Base URL:** `https://tools.cdc.gov/api`
- **Official documentation:** [Get Media Syndicated HTML](https://tools.cdc.gov/api/docs/info.aspx)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cssClasses` | query | `string` | no | Comma-delimited class IDs to retrieve from the source page. |
| `mediaId` | path | `number` | yes | The identifier of the media. |
| `stripScripts` | query | `boolean` | no | When true, JavaScript is stripped from the syndicated content. |
| `stripAnchors` | query | `boolean` | no | When true, anchor tags are stripped from the syndicated content. |
| `stripImages` | query | `boolean` | no | When true, images are stripped from the syndicated content. |
