# List Workspaces with Inistate

Finds workspaces in Inistate by name.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/workspace`
- **Base URL:** `https://api.inistate.com`
- **Official documentation:** [List Workspaces](https://app.swaggerhub.com/apis-docs/Inistate/InistateAPI/1.0.0)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `search` | query | `string` | no | Optional workspace-name search string. Leave blank to return all visible workspaces. |
