# List Related Tags with Centers for Disease Control and Prevention

Retrieves related tags from CDC Content Services.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/resources/tags/:tagId/related`
- **Base URL:** `https://tools.cdc.gov/api`
- **Official documentation:** [List Related Tags](https://tools.cdc.gov/api/docs/info.aspx)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `tagId` | path | `number` | yes | The identifier of the tag. |
