# List Data Stores with Make

Lists data stores for the specified team.

## Endpoint

- **Method:** `GET`
- **Path:** `/data-stores`
- **Base URL:** `https://us2.make.com/api/v2`
- **Official documentation:** [List Data Stores](https://developers.make.com/api-documentation/api-reference/data-stores)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `teamId` | query | `number` | yes | The ID of the Make team whose data stores should be listed. |
