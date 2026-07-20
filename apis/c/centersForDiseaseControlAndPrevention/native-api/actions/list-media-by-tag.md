# List Media By Tag with Centers for Disease Control and Prevention

Retrieves media by tag from CDC Content Services.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/resources/tags/:tagId/media`
- **Base URL:** `https://tools.cdc.gov/api`
- **Official documentation:** [List Media By Tag](https://tools.cdc.gov/api/docs/info.aspx)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `tagId` | path | `number` | yes | The identifier of the tag. |
