# Create Scenario Folder with Make

Creates a scenario folder in the specified team.

## Endpoint

- **Method:** `POST`
- **Path:** `/scenarios-folders`
- **Base URL:** `https://us2.make.com/api/v2`
- **Official documentation:** [Create Scenario Folder](https://developers.make.com/api-documentation/api-reference/scenarios-folders)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `teamId` | body | `number` | yes | The ID of the Make team in which to create the scenario folder. |
| `name` | body | `string` | yes | The name of the scenario folder to create. |
