# Create App Variable Group with Codemagic

Creates a new variable group for a Codemagic app.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v3/apps/:app_id/variable-groups`
- **Base URL:** `https://codemagic.io`
- **Official documentation:** [Create App Variable Group](https://codemagic.io/api/v3/schema#tag/Secrets%20and%20Environment%20Vars/operation/ApiV3AppsAppIdVariableGroupsCreateVariableGroup)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `app_id` | path | `string` | yes | Codemagic application identifier. |
| `name` | body | `string` | yes | Variable group name. Codemagic disallows periods and dollar signs. |
