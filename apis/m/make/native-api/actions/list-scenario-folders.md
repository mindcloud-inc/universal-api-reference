# List Scenario Folders with Make

Lists scenario folders for the specified team.

## Endpoint

- **Method:** `GET`
- **Path:** `/scenarios-folders`
- **Base URL:** `https://us2.make.com/api/v2`
- **Official documentation:** [List Scenario Folders](https://developers.make.com/api-documentation/api-reference/scenarios-folders)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `teamId` | query | `number` | yes | The ID of the Make team whose scenario folders should be listed. |
