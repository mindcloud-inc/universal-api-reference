# Get Import in Workspace with Microsoft Power BI

## Endpoint

- **Method:** `GET`
- **Path:** `groups/[:groupId]/imports/[:importId]`
- **Base URL:** `https://api.powerbi.com/v1.0/myorg`
- **Official documentation:** [Get Import in Workspace](https://learn.microsoft.com/en-us/rest/api/power-bi/imports/get-import-in-group)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `groupId` | path | `string` | yes | Power BI workspace ID that contains the import. |
| `importId` | path | `string` | yes | Power BI import ID to retrieve. |
